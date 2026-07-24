# AI623 DVLM — Exam Cheat Sheet

Open-book, Sun 24-May-2026, 15:00–18:00, SDSB B-3. No internet. Use Ctrl/Cmd+F to jump.

**Quick anchors:** [#numeric-tables](#numeric-tables) · [#diffusion](#diffusion) · [#ar-sampling](#ar-sampling) · [#attention](#attention) · [#alignment](#alignment) · [#vlm](#vlm) · [#reasoning](#reasoning) · [#solution-recipes](#solution-recipes) · [#sanity-checks](#sanity-checks) · [#pitfalls](#pitfalls)

---

## numeric-tables

**Natural log (ln):**
| x | ln x | x | ln x |
|---|---|---|---|
| 0.1 | −2.3026 | 0.6 | −0.5108 |
| 0.2 | −1.6094 | 0.667 | −0.4055 |
| 0.25 | −1.3863 | 0.7 | −0.3567 |
| 0.3 | −1.2040 | 0.8 | −0.2231 |
| 0.4 | −0.9163 | 0.9 | −0.1054 |
| 0.5 | −0.6931 | 1.4 | 0.3365 |
| 1.5 | 0.4055 | 2 | 0.6931 |
| e | 1.0000 | 10 | 2.3026 |

**e^x:**
| x | e^x | x | e^x |
|---|---|---|---|
| 0.05 | 1.0513 | 0.7071 | 2.0281 |
| 0.1 | 1.1052 | 1 | 2.7183 |
| 0.15 | 1.1618 | 2 | 7.3891 |
| 0.2 | 1.2214 | 3 | 20.086 |
| 0.4 | 1.4918 | 4 | 54.598 |
| 0.5 | 1.6487 | 5 | 148.41 |
| 0.6 | 1.8221 | −1 | 0.3679 |

**Sigmoid σ(x) = 1/(1+e^−x):**
| x | σ(x) |
|---|---|
| −1 | 0.2689 |
| −0.5 | 0.3775 |
| −0.15 | 0.4626 |
| −0.05 | 0.4875 |
| 0 | 0.5000 |
| 0.05 | 0.5125 |
| 0.15 | 0.5374 |
| 0.5 | 0.6225 |
| 1 | 0.7311 |
| 2 | 0.8808 |

**Square roots:**
| x | √x | x | √x |
|---|---|---|---|
| 0.1 | 0.3162 | 0.7 | 0.8367 |
| 0.2 | 0.4472 | 0.72 | 0.8485 |
| 0.28 | 0.5292 | 0.8 | 0.8944 |
| 0.3 | 0.5477 | 0.9 | 0.9487 |
| 0.4 | 0.6325 | 2 | 1.4142 |
| 0.5 | 0.7071 | 3 | 1.7321 |
| 0.504 | 0.7099 | 5 | 2.2361 |
| 0.6 | 0.7746 | 10 | 3.1623 |

---

## diffusion

### Forward process
- `α_t = 1 − β_t`,  `ᾱ_t = ∏_{i=1}^{t} α_i`  (monotonically decreasing in t)
- One-shot: `x_t = √ᾱ_t · x_0 + √(1−ᾱ_t) · ε`,  `ε ~ N(0, I)`
- Marginal: `q(x_t | x_0) = N(√ᾱ_t · x_0, (1−ᾱ_t) I)`
- SNR(t) = `ᾱ_t / (1−ᾱ_t)`

### True posterior q(x_{t−1} | x_t, x_0) = N(μ̃_t, β̃_t I)
- `β̃_t = ((1−ᾱ_{t−1}) / (1−ᾱ_t)) · β_t`   (always < β_t)
- `μ̃_t = (√ᾱ_{t−1}(1−α_t)/(1−ᾱ_t)) · x_0  +  (√α_t (1−ᾱ_{t−1})/(1−ᾱ_t)) · x_t`

### DDPM reverse step
```
μ_θ(x_t,t) = (1/√α_t) [ x_t − ((1−α_t)/√(1−ᾱ_t)) · ε_θ(x_t,t) ]
x_{t−1}    = μ_θ + σ_t · z,    z ~ N(0,I),    σ_t² = β̃_t  (or β_t)
```

### DDIM step (η blends DDPM↔DDIM; η=0 deterministic)
```
x̂_0   = (1/√ᾱ_t) [ x_t − √(1−ᾱ_t) · ε_θ ]
σ_t   = η · √((1−ᾱ_{t'})/(1−ᾱ_t)) · √(1 − ᾱ_t/ᾱ_{t'})
x_{t'} = √ᾱ_{t'} · x̂_0 + √(1−ᾱ_{t'} − σ_t²) · ε_θ + σ_t · z
```
- η=0: deterministic, no noise term, fewer steps OK.
- η=1, t'=t−1: reduces to DDPM (σ = √β̃_t).

### Score / NCSN
- Gaussian N(μ,v): `s(x) = −(x−μ)/v`
- Forward marginal score: `∇_{x_t} log q(x_t|x_0) = −ε / √(1−ᾱ_t)`
- DSM target: `∇_{x̃} log p_σ(x̃|x) = (x − x̃)/σ²`
- NCSN parameterization: `s_θ ≈ −ε/σ²`
- Per-sample DSM loss: `½ (ŝ − target)²`

### Flow Matching (linear interpolant)
- `x_t = t·x_1 + (1−t)·x_0`,  t ∈ [0,1]
- Target velocity (constant in t for fixed pair): `v = x_1 − x_0`
- CFM loss: `(v_θ − (x_1−x_0))²`
- Euler step: `x_{t+Δt} = x_t + Δt · v_θ`

### Classifier-Free Guidance
- `ε̂ = ε_θ(·,∅) + s · (ε_θ(·,c) − ε_θ(·,∅))`
- s=0 unconditional, s=1 conditional, s>1 extrapolation/sharpening.

### Noise schedules
- Linear: `β_t = β_1 + ((t−1)/(T−1))(β_T − β_1)`
- Cosine: `ᾱ_t = f(t)/f(0)`,  `f(t) = cos²((t/T+s)/(1+s) · π/2)`,  s=0.008

---

## ar-sampling

### Softmax + temperature
- `p_i = exp(z_i/T) / Σ_j exp(z_j/T)`
- T < 1 → sharper; T > 1 → flatter; T → 0: argmax; T → ∞: uniform.

### Top-k / Top-p
- **Top-k:** keep k largest p's, renormalize.
- **Top-p (nucleus):** sort desc, take smallest prefix with cumulative ≥ p, renormalize.

### Beam search
- Score = sum of `log p` along the path.
- Each step: extend each beam by every token, keep B best by cumulative log-prob.

### AR loss / perplexity
- Token NLL: `−log p(y_t | y_<t)`
- Avg loss `L = (1/T) Σ −log p(y_t|y_<t)`
- Perplexity: `PPL = exp(L)`

---

## attention

### Scaled dot-product attention
- `Attn(Q,K,V) = softmax(QKᵀ / √d_k) V`
- Shapes: Q ∈ R^{Lq×d}, K,V ∈ R^{Lk×d}, output R^{Lq×d}.

### Multi-head dims
- `d_k = d_v = d_model / h`
- W_Q, W_K, W_V, W_O each `d_model × d_model` ⇒ **4·d_model² params** (no biases).

### FLOPs / MACs
- QKᵀ: `L · L · d_model` MACs = `2 L² d_model` FLOPs.
- Attention·V: same `2 L² d_model` FLOPs.
- 4 linear projections: `4 · L · d_model²` MACs ≈ `8 L d_model²` FLOPs.
- Per-layer attn-only ≈ `4 L d_model² + 2 L² d_model` MACs (×2 for FLOPs).

### ViT
- Patches: `N = (H/P)(W/P)`,  L (with CLS) = `N + 1`.
- Patch-embed linear: in_dim `P·P·C`, out_dim D ⇒ params `(P²C)D + D` (with bias).

---

## alignment

### KL (discrete)
- `KL(π || π_ref) = Σ_a π(a) log[π(a)/π_ref(a)]`
- Always ≥ 0; zero iff π = π_ref.

### PPO clipped
- Ratio: `ρ_t = π_θ(a|s) / π_θ_old(a|s)`
- `L^CLIP_t = min(ρ_t Â_t, clip(ρ_t, 1−ε, 1+ε) Â_t)`
- If Â_t > 0 and ρ > 1+ε ⇒ clipped, gradient = 0.
- If Â_t < 0 and ρ < 1−ε ⇒ clipped, gradient = 0.
- Otherwise: gradient flows.

### DPO
```
m = β [ (log π_θ(y+) − log π_ref(y+)) − (log π_θ(y−) − log π_ref(y−)) ]
ℓ_DPO = −log σ(m)
```
- Mean over batch.
- Pair misranked (m<0) ⇒ ℓ > log 2 ≈ 0.693.

### GRPO
- Group rewards r_1..r_K (one prompt, K rollouts).
- Advantage per rollout: `Â_i = (r_i − mean(r)) / std(r)`  (population std unless told otherwise).
- Then PPO-style clipped surrogate with this Â (no value net).

### Reward model (Bradley-Terry)
- `L_RM = −log σ(r_ψ(x,y+) − r_ψ(x,y−))`

### KL-regularized optimum
- `π*(y|x) ∝ π_ref(y|x) · exp(r(x,y)/β)`

---

## vlm

### CLIP / InfoNCE
- Cosine sim (after L2-norm): `s = ûᵀv̂`,  with `û = u/‖u‖`.
- Scaled logit: `ℓ_ij = ûᵢᵀv̂_j / τ`  (τ small ⇒ sharp).
- One-direction loss (row i, image→text):
  `L^I→T_i = −log [ exp(ℓ_ii) / Σ_j exp(ℓ_ij) ]`
- Symmetric: `L = ½(L^I→T + L^T→I)`, each averaged over batch.
- Softmax gradient: `∂L/∂ℓ_ij = p_ij − 1{j=i}`.

### Cross-attention (text→image or image→text)
- Q from one modality, K,V from the other. Same formula as self-attention.

### LLaVA-style token budget
- Visual tokens = patch count from vision encoder (CLS may be dropped).
- `L_ctx = L_sys + 1 (img-start) + N_visual + 1 (img-end) + L_question + L_answer`
- Q-Former: fixed M visual tokens regardless of image res.

### Next-token VLM logits
- `ℓ_y = hᵀ e_y`,  `p(y|h) = exp(ℓ_y) / Σ_y' exp(ℓ_y')`

---

## reasoning

### Self-consistency (majority vote over K CoT)
- `p(answer = a) = (1/K) Σ_k 1{ans_k = a}`
- For probability "correct is strict majority", enumerate multinomial over (correct, wrong_1, wrong_2, ...) with `k > each wrong count`.

### Multinomial pmf
- `P(k_1,...,k_m) = (n! / Π k_i!) · Π p_i^{k_i}`

### IoU (visual grounding)
- Intersection box: `[max x1, max y1, min x2, min y2]`. If invalid (x2≤x1 or y2≤y1) ⇒ area 0.
- `IoU = inter / (areaA + areaB − inter)`

### CoT cost arithmetic
- Cost = N_samples · tokens_per_sample · cost_per_token.

---

## solution-recipes

### Recipe: DDPM forward — find x_t, q(x_t|x_0)
1. Compute α_t = 1 − β_t for each t.
2. Compute ᾱ_t by cumulative product.
3. Mean = √ᾱ_t · x_0;  Var = 1 − ᾱ_t.
4. If ε given: x_t = √ᾱ_t x_0 + √(1−ᾱ_t) ε.

### Recipe: DDPM reverse step
1. Need: α_t, ᾱ_t, ᾱ_{t−1}, x_t, ε_θ(x_t,t), z.
2. Compute 1/√α_t and (1−α_t)/√(1−ᾱ_t).
3. μ_θ = (1/√α_t)·(x_t − ((1−α_t)/√(1−ᾱ_t))·ε_θ).
4. σ_t² = β̃_t = ((1−ᾱ_{t−1})/(1−ᾱ_t))·β_t.
5. x_{t−1} = μ_θ + σ_t·z.

### Recipe: DDIM jump t → t' (with η)
1. Compute x̂_0 = (1/√ᾱ_t)(x_t − √(1−ᾱ_t)·ε_θ).
2. σ_t² = η²·((1−ᾱ_{t'})/(1−ᾱ_t))·(1 − ᾱ_t/ᾱ_{t'}).
3. x_{t'} = √ᾱ_{t'}·x̂_0 + √(1−ᾱ_{t'}−σ_t²)·ε_θ + σ_t·z.
4. η=0 ⇒ drop the σ·z term and √(...) simplifies to √(1−ᾱ_{t'}).

### Recipe: CFG + reverse step
1. ε̂ = ε_∅ + s·(ε_c − ε_∅).
2. Substitute ε̂ in place of ε_θ in DDPM/DDIM step.

### Recipe: Softmax with temperature
1. z' = z / T.
2. Subtract max(z') for numerical stability (if hand-computing this is rarely needed).
3. Exponentiate and normalize.

### Recipe: Top-p
1. Sort probs desc.
2. Walk cumulative; stop at first index where cumsum ≥ p.
3. Renormalize that prefix.

### Recipe: 2×2 / small attention
1. Compute S = QKᵀ (entry-wise dot products of Q rows with K rows).
2. Divide by √d_k.
3. Row-wise softmax.
4. Multiply weights by V (row vectors of V weighted by softmax row).

### Recipe: PPO clipped per-token loss
1. ρ = π_θ / π_old.
2. Clip range [1−ε, 1+ε]; ρ_c = clip(ρ).
3. If Â ≥ 0: L = min(ρ·Â, ρ_c·Â) = (min of ρ, ρ_c)·Â.
4. If Â < 0: L = min(ρ·Â, ρ_c·Â) = (max of ρ, ρ_c)·Â (because Â flips inequality).
5. Gradient is zero iff the clipped branch wins.

### Recipe: DPO loss on a batch
1. For each pair: Δ+ = log π_θ(y+) − log π_ref(y+); Δ− = log π_θ(y−) − log π_ref(y−).
2. m = β(Δ+ − Δ−).
3. ℓ = −log σ(m).  (Use sigmoid table.)
4. Mean over pairs.

### Recipe: GRPO advantage
1. r̄ = mean(rewards); s = std(rewards) (population: divide by K, not K−1, unless told).
2. Â_i = (r_i − r̄)/s.
3. Plug into PPO clipped surrogate with the right ρ for the token.

### Recipe: CLIP loss on batch
1. Build B×B logit matrix L_ij = ℓ scores (after L2 norm + ÷τ).
2. Row-softmax for image→text:  p_ij = exp(L_ij)/Σ_k exp(L_ik). Loss row i = −log p_ii.
3. Average. Column-softmax for text→image similarly.
4. Symmetric = ½(I→T + T→I).

### Recipe: ViT params / FLOPs
1. N = (H/P)(W/P).
2. L = N + 1 (CLS).
3. Patch-embed params = P²·C·D (+D bias).
4. Attn FLOPs per layer ≈ 2·(4 L D² + 2 L² D).

### Recipe: VLM token budget
1. Count visual tokens from encoder + projector.
2. Sum: BOS + sys + image-markers + visual + question + answer-so-far.

### Recipe: IoU
1. ix1 = max(Ax1,Bx1); iy1 = max(...); ix2 = min(...); iy2 = min(...).
2. If ix2≤ix1 or iy2≤iy1 ⇒ IoU=0.
3. Inter = (ix2−ix1)(iy2−iy1). Union = areaA + areaB − inter.

---

## sanity-checks

- **ᾱ_t** is decreasing in t (all α_i < 1).
- **β̃_t < β_t** always.
- **DDIM with η=1, t'=t−1 ≡ DDPM.**
- **σ ↔ ε:** s = −ε/σ² for NCSN.
- **Flow-matching v_target** is constant in t for a fixed (x_0, x_1) pair (straight line).
- **Softmax temperature:** small T ⇒ sharper.
- **KL ≥ 0**; check by Jensen if a problem gives negative answer, you have a sign error.
- **DPO logit margin m**: positive ⇒ pair correctly ranked ⇒ loss < log 2 (≈0.693).
- **PPO ratio**: ρ=1 ⇒ on-policy ⇒ surrogate = Â.
- **GRPO**: if all K rewards equal ⇒ std=0 ⇒ advantage undefined ⇒ skip (or add ε).
- **CLIP loss lower bound** = log B (perfect alignment) → actually `−log 1 = 0` for full-prob assignment; the practical min is `≈ 0` when diagonals dominate.
- **CLIP loss upper bound** ≈ log B (uniform softmax).
- **IoU ∈ [0,1]**; identical boxes ⇒ 1.0.
- **Cosine sim ∈ [−1, 1]** after L2-norm.
- **Total prob mass = 1** after any softmax / renorm.

---

## pitfalls

- **β_t vs ᾱ_t:** β_t is per-step variance; ᾱ_t is the cumulative product of α's. Don't confuse.
- **σ_t in DDPM:** can be β_t **or** β̃_t (Ho et al. allow both). Use what the problem specifies; default β̃_t.
- **Log base:** unless told otherwise, use **natural log** for ML losses, KL, perplexity. PPL uses `e^L`.
- **Top-p edge case:** if first token already exceeds p, you keep just that one token.
- **PPO clip with Â<0:** min flips — be careful with sign.
- **DPO:** uses `log π` directly (sum over tokens), not probabilities.
- **GRPO std:** population by default; if told sample std, divide by K−1.
- **CLIP τ:** small τ amplifies logits — sharp softmax, big gradients early in training.
- **ViT CLS:** sometimes dropped before LM (LLaVA). Check the problem.
- **Attention dims:** Q comes from the "querier" modality; K,V from the "queried." For cross-attn text→image, Q from text.
- **IoU:** be defensive — check for negative intersection.
- **Self-consistency tie-breaking:** read the rule carefully (favor correct? uniform? lowest label?).
- **Flow matching:** the loss is over **velocity**, not over the noisy point. Don't square (x_t − target).
- **Always include the CLS token** in ViT sequence length unless told otherwise (`L = N+1`).
- **Patch-embed params:** include bias if asked, exclude otherwise.
- **Exam time budget:** 3 hours / ~25 problems → ~7 min each. If stuck >10 min, mark and move on.

---

## time-budget hint (exam day)

- ~60 min / topic → ~6–8 min / problem.
- First pass: solve the easy 60% across all 3 topics. Second pass: hard ones.
- Diffusion problems are the most arithmetic-heavy — do them when fresh.
- Open-book reality: search this file first (Ctrl+F a formula name); then your lecture PDFs only if missing.

