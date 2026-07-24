# Topic 3 — Vision-Language Models (VLM) + Reasoning

Practice bank for AI623 final (Sun 24-May-2026). Style calibrated to PA3-Quiz Q1 (projector / fused-hidden / softmax) and PA3 analytical problems (CLIP InfoNCE, Q-Former, gated cross-attention, parameter counts).

---

## Topic scope & key formulas

**ViT patch tokenization**
- Number of spatial patches: `N = (H/P) · (W/P)`
- Sequence length with CLS: `L = N + 1`
- Patch-embedding linear layer params (with bias): `(P · P · C) · D + D`
- Per-token self-attention FLOPs (one layer, one head): `~ 4 L D² + 2 L² D`

**CLIP / contrastive learning**
- Cosine similarity (assumes `‖u‖=‖v‖=1`): `s = uᵀv`
- Scaled logit: `ℓ_ij = uᵢᵀ vⱼ / τ`
- CLIP symmetric loss (one direction): `L_{I→T}^{(i)} = − log [ exp(ℓ_ii) / Σⱼ exp(ℓ_ij) ]`
- Full symmetric: `L = ½(L_{I→T} + L_{T→I})`
- InfoNCE decomposition: `L = −E[s_ii] + E[log Σⱼ e^{s_ij}]`  (alignment + uniformity)
- Gradient: `∂L/∂ℓ_ij = p_ij − 1{j=i}` with `p_ij = exp(ℓ_ij)/Σ_k exp(ℓ_ik)`

**Cross / multimodal attention**
- `Attn(Q,K,V) = softmax(Q Kᵀ / √d) V`, shapes: `Q ∈ R^{Lq×d}, K,V ∈ R^{Lk×d}`
- Output shape: `R^{Lq×d}`

**VLM fusion / token budget**
- LLaVA-style total context: `L_ctx = L_sys + N_img_tokens + L_text + L_answer`
- Q-Former: LM receives exactly `M` visual tokens (resolution-agnostic)
- Logit `ℓ_y = hᵀ e_y`; softmax `p(y|h) = exp(ℓ_y) / Σ_y' exp(ℓ_y')`

**Visual reasoning grounding**
- IoU = `|A ∩ B| / |A ∪ B|`
- Self-consistency: `p(answer = a) = (1/K) Σ_k 1{ans_k = a}` over K reasoning chains

---

## Problem 1: ViT patch count & token sequence

**Given:** Image size `H × W × C = 224 × 224 × 3`. Patch size `P = 16`. The ViT prepends one [CLS] token. Embedding dimension `D = 768`. The patch-embedding layer is a linear projection from a flattened patch (with bias).

**Find:**
(a) number of spatial patches `N`;
(b) full token sequence length `L`;
(c) trainable parameters in the patch-embedding linear layer.

**Solution:**

(a) Patches per side = `224 / 16 = 14`.
`N = 14 × 14 = 196`.

(b) With one prepended CLS token:
`L = N + 1 = 196 + 1 = 197`.

(c) Each patch flattens to `P·P·C = 16·16·3 = 768` numbers. The linear layer maps `768 → D=768` with bias.

- Weight params: `768 × 768 = 589,824`
- Bias params: `768`
- Total: `589,824 + 768 = 590,592`

**Answer:**
- (a) **N = 196**
- (b) **L = 197**
- (c) **590,592 parameters**

---

## Problem 2: ViT FLOP estimate for self-attention

**Given:** A single ViT self-attention layer (single head, for simplicity) operating on `L = 197` tokens with hidden dim `D = 768`. Use the approximation:

`FLOPs_layer ≈ 4·L·D² (QKV+output projections) + 2·L²·D (attention scores + weighted sum)`

The model has `n_layers = 12` such layers. Ignore MLP / LayerNorm cost.

**Find:** Total attention-only FLOPs across all 12 layers (give in GFLOPs to 2 dp).

**Solution:**

Step 1 — QKV+output projections per layer:
`4 · L · D² = 4 · 197 · 768² = 4 · 197 · 589,824`
`= 788 · 589,824 = 464,781,312` FLOPs

Step 2 — attention score and weighted sum per layer:
`2 · L² · D = 2 · 197² · 768 = 2 · 38,809 · 768`
`= 77,618 · 768 = 59,610,624` FLOPs

Step 3 — per-layer total:
`464,781,312 + 59,610,624 = 524,391,936` FLOPs ≈ `0.5244` GFLOPs

Step 4 — across 12 layers:
`12 · 524,391,936 = 6,292,703,232` FLOPs

Convert to GFLOPs: `6,292,703,232 / 1e9 ≈ 6.2927` GFLOPs.

**Answer:** **≈ 6.29 GFLOPs**

---

## Problem 3: Cosine similarity & temperature-scaled logits

**Given:** Two CLIP encoders produce, for one image-text pair, the un-normalised vectors
`u = (3, 4)` (image), `v = (1, 2)` (text). Temperature `τ = 0.1`.

**Find:**
(a) the cosine similarity `s = ûᵀv̂` after L2-normalisation;
(b) the scaled logit `ℓ = s / τ`;
(c) repeat (b) with `τ = 1.0` and comment on which τ gives a sharper softmax.

**Solution:**

(a) Norms:
`‖u‖ = √(9+16) = √25 = 5`,  `‖v‖ = √(1+4) = √5 ≈ 2.2361`
Normalised vectors:
`û = (3/5, 4/5) = (0.6, 0.8)`
`v̂ = (1/√5, 2/√5) ≈ (0.4472, 0.8944)`
Cosine similarity:
`s = 0.6·0.4472 + 0.8·0.8944 = 0.26833 + 0.71554 = 0.98387`

(b) `ℓ = s / τ = 0.98387 / 0.1 = 9.8387`

(c) With `τ = 1.0`: `ℓ = 0.98387`.
Lower τ (0.1) magnifies the logit roughly 10× → softmax becomes much sharper (closer to one-hot), so τ=0.1 gives the sharper distribution.

**Answer:** **s ≈ 0.9839, ℓ(τ=0.1) ≈ 9.8387, ℓ(τ=1.0) ≈ 0.9839; τ=0.1 yields the sharper softmax.**

---

## Problem 4: CLIP contrastive loss on a 3-pair batch

**Given:** A CLIP batch of `B = 3` matched image-text pairs already produces the scaled logit matrix (rows = images, columns = texts) `L_ij = uᵢᵀvⱼ/τ`:

```
        t1     t2     t3
i1  [  2.0    0.5    0.0  ]
i2  [  0.0    2.0    1.0  ]
i3  [  1.0    0.0    2.0  ]
```

The diagonal is the matched pair. Compute the image-to-text CLIP loss

`L_{I→T} = (1/B) Σᵢ −log [ exp(ℓ_ii) / Σⱼ exp(ℓ_ij) ]`

(Use `e ≈ 2.7183`, `e² ≈ 7.3891`, `e^0.5 ≈ 1.6487`, `e^0 = 1`, `e^1 ≈ 2.7183`.)

**Find:** `L_{I→T}` to 4 dp.

**Solution:**

Row i=1: exponentials of (2.0, 0.5, 0.0)
- `e^2 = 7.3891`, `e^0.5 = 1.6487`, `e^0 = 1.0000`
- Sum = `7.3891 + 1.6487 + 1.0000 = 10.0378`
- `p_11 = 7.3891 / 10.0378 = 0.7361`
- `−log p_11 = −log(0.7361) = 0.3065`

Row i=2: exponentials of (0.0, 2.0, 1.0)
- `e^0 = 1.0000`, `e^2 = 7.3891`, `e^1 = 2.7183`
- Sum = `1.0000 + 7.3891 + 2.7183 = 11.1074`
- `p_22 = 7.3891 / 11.1074 = 0.6653`
- `−log p_22 = 0.4076`

Row i=3: exponentials of (1.0, 0.0, 2.0)
- `e^1 = 2.7183`, `e^0 = 1.0000`, `e^2 = 7.3891`
- Sum = `2.7183 + 1.0000 + 7.3891 = 11.1074`
- `p_33 = 7.3891 / 11.1074 = 0.6653`
- `−log p_33 = 0.4076`

Average:
`L_{I→T} = (0.3065 + 0.4076 + 0.4076) / 3 = 1.1217 / 3 = 0.3739`

**Answer:** **L_{I→T} ≈ 0.3739**

---

## Problem 5: Cross-attention from text query to image keys/values

**Given:** A text query attends to 3 image-patch tokens. Hidden dim `d = 2`. (Already-projected) matrices:

`Q = [1, 0]`  (one query, shape 1×2)

`K = [[1, 0],
      [0, 1],
      [1, 1]]`  (3×2)

`V = [[1, 2],
      [3, 4],
      [5, 6]]`  (3×2)

Use scaled dot-product attention `softmax(Q Kᵀ / √d) · V` with `√d = √2 ≈ 1.4142`.

**Find:** The output vector (1×2) and the attention weights.

**Solution:**

Step 1 — raw scores `Q Kᵀ`:
`Q · K_1ᵀ = 1·1 + 0·0 = 1`
`Q · K_2ᵀ = 1·0 + 0·1 = 0`
`Q · K_3ᵀ = 1·1 + 0·1 = 1`
Raw scores = `(1, 0, 1)`.

Step 2 — scaled scores (÷√2):
`(1/√2, 0/√2, 1/√2) = (0.7071, 0, 0.7071)`

Step 3 — softmax:
`e^0.7071 ≈ 2.0281`, `e^0 = 1.0000`, `e^0.7071 ≈ 2.0281`
Sum = `2.0281 + 1.0000 + 2.0281 = 5.0562`
Weights = `(2.0281/5.0562, 1.0000/5.0562, 2.0281/5.0562)`
       ≈ `(0.4011, 0.1978, 0.4011)`
(Check: `0.4011 + 0.1978 + 0.4011 = 1.0000` ✓)

Step 4 — weighted sum of `V`:
- Component 1: `0.4011·1 + 0.1978·3 + 0.4011·5`
             = `0.4011 + 0.5934 + 2.0055 = 3.0000`
- Component 2: `0.4011·2 + 0.1978·4 + 0.4011·6`
             = `0.8022 + 0.7912 + 2.4066 = 4.0000`

**Answer:** **Output = (3.0000, 4.0000); attention weights ≈ (0.4011, 0.1978, 0.4011).**

---

## Problem 6: LLaVA-style token budget + next-token probability

**Given:** A LLaVA-style VLM with:
- CLIP ViT-B/32 vision encoder: image `224×224`, patch `32×32`, CLS discarded.
- MLP projector outputs one LM token per spatial patch (no token reduction).
- LM context = `[BOS] + [system_prompt (10 tokens)] + [<image>] + visual_tokens + [</image>] + [user_question (12 tokens)] + [answer_so_far]`.

The LM has just produced the visual-conditioned hidden state `h ∈ R³` for the next position:

`h = (0.4, 0.6, 0.2)`

Candidate answer tokens with LM embeddings:
`e_yes  = (1, 0, 0)`,   `e_no   = (0, 1, 0)`,   `e_maybe = (0, 0, 1)`.

Logits `ℓ_y = hᵀ e_y`; probabilities via softmax over {yes, no, maybe}.

**Find:**
(a) number of visual tokens that enter the LM;
(b) total context length **before** any answer token is generated;
(c) softmax probability of token `no`.

**Solution:**

(a) Patches per side: `224 / 32 = 7`. Visual-patch count = `7 × 7 = 49`. CLS discarded → **49 visual tokens** reach the LM.

(b) Total prefix (no answer yet, so `L_answer = 0`):
`L_ctx = 1 (BOS) + 10 (sys) + 1 (<image>) + 49 (visual) + 1 (</image>) + 12 (question)`
`     = 1 + 10 + 1 + 49 + 1 + 12 = 74` tokens.

(c) Logits:
`ℓ_yes   = 0.4·1 + 0.6·0 + 0.2·0 = 0.4`
`ℓ_no    = 0.4·0 + 0.6·1 + 0.2·0 = 0.6`
`ℓ_maybe = 0.4·0 + 0.6·0 + 0.2·1 = 0.2`

Exponentials:
`e^0.4 ≈ 1.4918`, `e^0.6 ≈ 1.8221`, `e^0.2 ≈ 1.2214`
Sum = `1.4918 + 1.8221 + 1.2214 = 4.5353`

`p(no | h) = 1.8221 / 4.5353 = 0.4018`

**Answer:**
- (a) **49 visual tokens**
- (b) **L_ctx = 74 tokens**
- (c) **p(no | h) ≈ 0.4018**

---

## Problem 7: Visual reasoning — self-consistency + grounding IoU

**Given:** A VLM is asked "Where is the cat, and how many cats are there?" It is sampled `K = 5` independent chain-of-thought traces. Each trace returns (answer_count, predicted_bbox). The ground-truth bbox is `G = [x1=10, y1=10, x2=50, y2=50]` (area = 40·40 = 1600).

| chain k | answer (count) | predicted bbox `[x1,y1,x2,y2]` |
|---|---|---|
| 1 | 1 | [10, 10, 50, 50] |
| 2 | 1 | [20, 10, 60, 50] |
| 3 | 2 | [10, 20, 50, 60] |
| 4 | 1 | [15, 15, 55, 55] |
| 5 | 1 | [10, 10, 50, 50] |

**Find:**
(a) the self-consistency answer (majority vote) and `p(answer = 1)` across the 5 chains;
(b) the IoU of chain 2's bbox with the ground truth;
(c) the **mean IoU** across all 5 chains (use IoU for the boxes in chains 1, 3, 4, 5 too).

**Solution:**

(a) Counts of answers: `1` appears in chains {1,2,4,5} → 4 times; `2` appears in chain {3} → 1 time.
Majority = `1`. `p(answer=1) = 4/5 = 0.80`.

(b) Chain 2 box `B = [20,10,60,50]`. Intersection with `G = [10,10,50,50]`:
- ix1 = max(10,20) = 20;  iy1 = max(10,10) = 10
- ix2 = min(50,60) = 50;  iy2 = min(50,50) = 50
- Intersection w = 50−20 = 30, h = 50−10 = 40 → area = `30·40 = 1200`
- Area(G) = 1600;  Area(B) = (60−20)·(50−10) = 40·40 = 1600
- Union = `1600 + 1600 − 1200 = 2000`
- IoU₂ = `1200 / 2000 = 0.6000`

Now the others:

Chain 1: B = [10,10,50,50] = G exactly. IoU₁ = 1600/1600 = **1.0000**.

Chain 3: B = [10,20,50,60]. Intersection with G = [10,10,50,50]:
- ix1=10, iy1=20, ix2=50, iy2=50 → w=40, h=30, area=1200
- Area(B) = 40·40 = 1600;  Union = 1600+1600−1200 = 2000
- IoU₃ = 1200/2000 = **0.6000**

Chain 4: B = [15,15,55,55]. Intersection with G = [10,10,50,50]:
- ix1=15, iy1=15, ix2=50, iy2=50 → w=35, h=35, area=1225
- Area(B) = 40·40 = 1600;  Union = 1600+1600−1225 = 1975
- IoU₄ = 1225/1975 ≈ **0.6203**

Chain 5: same as chain 1 → IoU₅ = **1.0000**.

(c) Mean IoU:
`(1.0000 + 0.6000 + 0.6000 + 0.6203 + 1.0000) / 5`
`= 3.8203 / 5 = 0.7641`

**Answer:**
- (a) **self-consistency answer = 1; p(answer=1) = 0.80**
- (b) **IoU (chain 2) = 0.6000**
- (c) **Mean IoU ≈ 0.7641**
