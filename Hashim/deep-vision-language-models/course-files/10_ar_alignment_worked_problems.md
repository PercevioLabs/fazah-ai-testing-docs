# AR Text Generation + Alignment (RLHF/PPO/DPO/GRPO) + Reasoning — Practice Problems

## Topic scope & key formulas

1. **Softmax with temperature:** $p_i = \dfrac{\exp(z_i/T)}{\sum_j \exp(z_j/T)}$
2. **Top-p (nucleus):** smallest set $V_p$ with $\sum_{i\in V_p} p_{(i)} \ge p$ (sorted desc), then renormalize.
3. **Scaled dot-product attention:** $\text{Attn}(Q,K,V) = \text{softmax}\!\left(\dfrac{QK^\top}{\sqrt{d_k}}\right)V$
4. **MHA dims:** $d_k = d_v = d_\text{model}/h$; params per attention block $= 4 d_\text{model}^2$ (Q,K,V,O).
5. **AR cross-entropy / perplexity:** $\mathcal{L} = -\dfrac{1}{T}\sum_{t=1}^{T} \log p(y_t\mid y_{<t})$, $\text{PPL} = e^{\mathcal{L}}$.
6. **KL divergence (discrete):** $\text{KL}(\pi\|\pi_\text{ref}) = \sum_a \pi(a)\log\dfrac{\pi(a)}{\pi_\text{ref}(a)}$
7. **PPO clipped objective:** $L^\text{CLIP}_t = \min\!\big(\rho_t \hat A_t,\ \text{clip}(\rho_t, 1-\varepsilon, 1+\varepsilon)\hat A_t\big)$, with $\rho_t = \dfrac{\pi_\theta(a_t|s_t)}{\pi_{\theta_\text{old}}(a_t|s_t)}$.
8. **DPO loss:** $\ell_\text{DPO} = -\log\sigma\!\left(\beta\log\dfrac{\pi_\theta(y^+|x)}{\pi_\text{ref}(y^+|x)} - \beta\log\dfrac{\pi_\theta(y^-|x)}{\pi_\text{ref}(y^-|x)}\right)$
9. **GRPO group advantage:** $\hat A_i = \dfrac{r_i - \text{mean}(\{r_j\})}{\text{std}(\{r_j\})}$ over the $K$ group completions.
10. **Bradley-Terry reward-model log-likelihood:** $\mathcal{L}_\text{RM} = -\log\sigma(r_\psi(x,y^+) - r_\psi(x,y^-))$
11. **Optimal KL-regularized policy:** $\pi^*(y|x) \propto \pi_\text{ref}(y|x)\exp(r(x,y)/\beta)$

---

### Problem 1: Temperature softmax
**Given:** Logits over a 3-token vocabulary $\{A,B,C\}$ are $z = (2.0,\ 1.0,\ 0.0)$. Temperature $T=0.5$.
**Find:** The sampling distribution $p$.

**Solution:**
Step 1. Scale: $z/T = (4.0,\ 2.0,\ 0.0)$.
Step 2. Exponentiate: $e^{4}=54.598$, $e^{2}=7.389$, $e^{0}=1.000$.
Step 3. Sum: $Z = 54.598+7.389+1.000 = 62.987$.
Step 4. Normalize:
- $p_A = 54.598/62.987 = 0.8668$
- $p_B = 7.389/62.987 = 0.1173$
- $p_C = 1.000/62.987 = 0.0159$

**Answer:** $\boxed{p \approx (0.867,\ 0.117,\ 0.016)}$

---

### Problem 2: Top-k vs Top-p with beam-search step
**Given:** Vocab $\{w_1,\dots,w_5\}$ with probabilities $p = (0.40,\ 0.25,\ 0.15,\ 0.12,\ 0.08)$.
**Find:** (a) Top-k=3 renormalized distribution. (b) Top-p set for $p=0.80$ and renormalized distribution. (c) In a beam search with beam width $B=2$, current beams have cumulative log-probs $\log(0.5)=-0.693$ and $\log(0.3)=-1.204$. Extending each beam by all 5 tokens above, what are the top-2 cumulative log-probs after the step?

**Solution:**
(a) Top-3 = $\{w_1,w_2,w_3\}$, masses $0.40+0.25+0.15=0.80$. Renormalize:
- $(0.40,0.25,0.15)/0.80 = (0.500,\ 0.3125,\ 0.1875)$.

(b) Cumulative sums (sorted desc): $0.40, 0.65, 0.80$. Smallest set with cumulative $\ge 0.80$ is $\{w_1,w_2,w_3\}$, mass 0.80. Same renormalized as in (a): $(0.500, 0.3125, 0.1875)$.

(c) For beam 1 ($\log P_1=-0.693$): extensions add $\log p_i$. Best two: $w_1: -0.693 + \log 0.40 = -0.693 -0.916 = -1.609$; $w_2: -0.693 -1.386 = -2.079$.
For beam 2 ($\log P_2=-1.204$): $w_1: -1.204 -0.916 = -2.120$; $w_2: -1.204 -1.386 = -2.590$.
All candidates sorted: $-1.609, -2.079, -2.120, -2.590, \dots$
Top-2 kept: $-1.609$ (beam1+$w_1$) and $-2.079$ (beam1+$w_2$).

**Answer:** (a) $\boxed{(0.500,\ 0.3125,\ 0.1875)}$; (b) set $\{w_1,w_2,w_3\}$, $\boxed{(0.500,\ 0.3125,\ 0.1875)}$; (c) $\boxed{-1.609,\ -2.079}$.

---

### Problem 3: Scaled dot-product attention on a 2x2 example
**Given:** Single head, $d_k=2$, sequence length 2.
$Q = \begin{pmatrix}1 & 0\\ 0 & 1\end{pmatrix}$, $K = \begin{pmatrix}1 & 1\\ 1 & 0\end{pmatrix}$, $V = \begin{pmatrix}1 & 2\\ 3 & 4\end{pmatrix}$.
**Find:** The attention output matrix.

**Solution:**
Step 1. $QK^\top$: row1 of Q is $(1,0)$; dot with rows of K: $(1\cdot1+0\cdot1,\ 1\cdot1+0\cdot0)=(1,1)$. Row2 of Q is $(0,1)$: $(0\cdot1+1\cdot1,\ 0\cdot1+1\cdot0)=(1,0)$.
$QK^\top = \begin{pmatrix}1 & 1\\ 1 & 0\end{pmatrix}$.

Step 2. Divide by $\sqrt{d_k}=\sqrt2 \approx 1.4142$: scores $= \begin{pmatrix}0.7071 & 0.7071\\ 0.7071 & 0\end{pmatrix}$.

Step 3. Row-wise softmax.
- Row1: identical logits → $(0.5, 0.5)$.
- Row2: $e^{0.7071}=2.0281$, $e^{0}=1$, sum $=3.0281$. Weights $(0.6698, 0.3302)$.

Step 4. Multiply by $V$.
- Row1: $0.5\cdot(1,2) + 0.5\cdot(3,4) = (2.0, 3.0)$.
- Row2: $0.6698\cdot(1,2) + 0.3302\cdot(3,4) = (0.6698+0.9906,\ 1.3396+1.3208) = (1.6604, 2.6604)$.

**Answer:** $\boxed{\text{Attn} \approx \begin{pmatrix}2.000 & 3.000\\ 1.660 & 2.660\end{pmatrix}}$

---

### Problem 4: Parameter & FLOP count for multi-head attention
**Given:** A transformer block with $d_\text{model}=512$, $h=8$ heads, sequence length $L=128$.
**Find:** (a) Per-head $d_k$. (b) Total parameter count for the four projections $W_Q,W_K,W_V,W_O$ (ignore biases). (c) FLOPs (multiply-adds counted as 2 ops) for computing $QK^\top$ alone for one sample.

**Solution:**
(a) $d_k = 512/8 = 64$.

(b) Each of $W_Q,W_K,W_V,W_O$ is $d_\text{model}\times d_\text{model} = 512\times512 = 262{,}144$. Total $=4\times 262{,}144 = 1{,}048{,}576 \approx 1.05$M.

(c) $QK^\top$: $Q \in \mathbb{R}^{L\times d_\text{model}}$, $K^\top \in \mathbb{R}^{d_\text{model}\times L}$. Output is $L\times L$ requiring $L\cdot L\cdot d_\text{model}$ multiply-adds.
$= 128 \cdot 128 \cdot 512 = 8{,}388{,}608$ MAC.
In FLOPs (2 per MAC): $2\cdot 8{,}388{,}608 = 16{,}777{,}216 \approx 1.68\times 10^{7}$ FLOPs.

**Answer:** (a) $\boxed{d_k=64}$; (b) $\boxed{1{,}048{,}576\ \text{params}}$; (c) $\boxed{\approx 1.68\times 10^{7}\ \text{FLOPs}}$.

---

### Problem 5: Cross-entropy and perplexity on a token sequence
**Given:** A 4-token target sequence with model-assigned probabilities to the correct next tokens: $p_1=0.5,\ p_2=0.25,\ p_3=0.10,\ p_4=0.40$.
**Find:** Average cross-entropy (nats) and perplexity.

**Solution:**
Step 1. Log-probs (natural log):
- $\ln 0.5 = -0.6931$
- $\ln 0.25 = -1.3863$
- $\ln 0.10 = -2.3026$
- $\ln 0.40 = -0.9163$

Step 2. Sum $= -(0.6931+1.3863+2.3026+0.9163) = -5.2983$. (i.e. NLL sum = 5.2983)

Step 3. Average loss $\mathcal{L} = 5.2983/4 = 1.3246$ nats/token.

Step 4. Perplexity $= e^{1.3246} = 3.761$.

**Answer:** $\boxed{\mathcal{L}=1.3246\ \text{nats},\ \text{PPL}\approx 3.76}$

---

### Problem 6: PPO clipped surrogate (single token)
**Given:** For a token $a_t$: $\pi_{\theta_\text{old}}(a_t|s_t)=0.40$, $\pi_\theta(a_t|s_t)=0.60$, advantage $\hat A_t = +2.0$, clip $\varepsilon=0.2$.
**Find:** The per-token PPO clipped surrogate loss value $L^\text{CLIP}_t$, and whether the gradient is active.

**Solution:**
Step 1. Ratio $\rho_t = 0.60/0.40 = 1.50$.
Step 2. Clip range: $[1-0.2,\ 1+0.2] = [0.8,\ 1.2]$. Clipped ratio $= 1.20$.
Step 3. Two candidates (since $\hat A_t > 0$):
- Unclipped term: $\rho_t \hat A_t = 1.50 \cdot 2.0 = 3.00$.
- Clipped term: $1.20 \cdot 2.0 = 2.40$.
Step 4. $L^\text{CLIP}_t = \min(3.00,\ 2.40) = 2.40$.
Step 5. Since the min is the clipped branch and $\rho_t$ is outside the clip range with $\hat A_t>0$, the gradient w.r.t. $\theta$ is zero (clipped region).

**Answer:** $\boxed{L^\text{CLIP}_t = 2.40,\ \text{gradient} = 0}$

---

### Problem 7: PPO with explicit KL penalty term
**Given:** Three-token vocab. Reference policy at state $s$: $\pi_\text{ref} = (0.5,\ 0.3,\ 0.2)$. Current policy: $\pi_\theta = (0.7,\ 0.2,\ 0.1)$. KL coefficient $\beta = 0.1$. The (unpenalized) expected task reward at this state is $\bar r = 1.20$.
**Find:** (a) $\text{KL}(\pi_\theta\|\pi_\text{ref})$ in nats. (b) The KL-shaped per-step objective value $J = \bar r - \beta\,\text{KL}$.

**Solution:**
Step 1. Compute ratios and logs.
- $\log(0.7/0.5) = \log 1.4 = 0.3365$
- $\log(0.2/0.3) = \log 0.6667 = -0.4055$
- $\log(0.1/0.2) = \log 0.5 = -0.6931$

Step 2. KL $= \sum_a \pi_\theta(a)\log\frac{\pi_\theta(a)}{\pi_\text{ref}(a)}$
$= 0.7(0.3365) + 0.2(-0.4055) + 0.1(-0.6931)$
$= 0.2356 - 0.0811 - 0.0693$
$= 0.0852$ nats.

Step 3. $J = 1.20 - 0.1 \cdot 0.0852 = 1.20 - 0.00852 = 1.1915$.

**Answer:** $\boxed{\text{KL} \approx 0.0852,\ J \approx 1.1915}$

---

### Problem 8: DPO loss on two preference pairs
**Given:** Two preference pairs, $\beta = 0.1$. For each, we have log-probs (sum over tokens) under $\pi_\theta$ and $\pi_\text{ref}$.

| pair | $\log\pi_\theta(y^+)$ | $\log\pi_\text{ref}(y^+)$ | $\log\pi_\theta(y^-)$ | $\log\pi_\text{ref}(y^-)$ |
|---|---|---|---|---|
| 1 | $-5.0$ | $-6.0$ | $-7.0$ | $-6.5$ |
| 2 | $-4.0$ | $-4.5$ | $-3.0$ | $-4.0$ |

**Find:** The mean DPO loss over the two pairs.

**Solution:**
Step 1. Compute per-pair logit margin $m = \beta[(\log\pi_\theta(y^+) - \log\pi_\text{ref}(y^+)) - (\log\pi_\theta(y^-) - \log\pi_\text{ref}(y^-))]$.

Pair 1:
- $\Delta^+ = -5.0 - (-6.0) = +1.0$
- $\Delta^- = -7.0 - (-6.5) = -0.5$
- $m_1 = 0.1\,(1.0 - (-0.5)) = 0.1 \cdot 1.5 = 0.15$
- $\sigma(0.15) = 1/(1+e^{-0.15}) = 1/(1+0.8607) = 0.5374$
- $\ell_1 = -\log 0.5374 = 0.6213$

Pair 2:
- $\Delta^+ = -4.0 - (-4.5) = +0.5$
- $\Delta^- = -3.0 - (-4.0) = +1.0$
- $m_2 = 0.1\,(0.5 - 1.0) = -0.05$
- $\sigma(-0.05) = 1/(1+e^{0.05}) = 1/(1+1.0513) = 0.4875$
- $\ell_2 = -\log 0.4875 = 0.7181$

Step 2. Mean loss $= (0.6213+0.7181)/2 = 1.3394/2 = 0.6697$.

**Answer:** $\boxed{\bar\ell_\text{DPO} \approx 0.6697}$ (pair 1: $0.6213$, pair 2: $0.7181$ — pair 2 is misranked, hence loss > $\log 2$).

---

### Problem 9: GRPO group-relative advantage and surrogate
**Given:** For one prompt, $K=4$ rollouts received rewards $r = (1.0,\ 0.0,\ 1.0,\ 0.0)$ (verifiable 0/1 reward, e.g. GSM8K). For a specific token in rollout 1: $\pi_{\theta_\text{old}}(a)=0.20$, $\pi_\theta(a)=0.30$, clip $\varepsilon = 0.2$. Use population std (divide by $K$).
**Find:** (a) Group-normalized advantage of rollout 1. (b) The PPO-style clipped surrogate value at this token (no KL term).

**Solution:**
Step 1. Mean $\bar r = (1+0+1+0)/4 = 0.5$.
Step 2. Variance (population) $= \frac{1}{4}\sum(r_i-\bar r)^2 = \frac{1}{4}(0.25+0.25+0.25+0.25) = 0.25$. Std $= 0.5$.
Step 3. $\hat A_1 = (1.0 - 0.5)/0.5 = +1.0$. (Same advantage for all rollouts within the group, by symmetry.)
Step 4. Ratio $\rho = 0.30/0.20 = 1.50$. Clipped range $[0.8,1.2]$; clipped $\rho = 1.20$.
Step 5. Surrogate $= \min(1.50\cdot 1.0,\ 1.20\cdot 1.0) = \min(1.50, 1.20) = 1.20$.

**Answer:** $\boxed{\hat A_1 = +1.0,\ L^\text{GRPO}_t = 1.20}$ (clipped, gradient zero on this token).

---

### Problem 10: Self-consistency majority vote with chain-of-thought budget
**Given:** A reasoning model samples $N=5$ independent chain-of-thought solutions to a math problem. Each sample is independently correct with probability $p=0.6$, and when wrong it outputs one of two distinct wrong answers uniformly at random (so each wrong-answer label has probability $0.2$). The model takes a majority vote (ties broken by picking the correct label only if it ties; otherwise pick uniformly at random among the tied top labels). Additionally, each CoT uses on average 180 tokens, and decoding cost is $c=2.5\times 10^{-6}$ USD/token.
**Find:** (a) Probability that the correct answer is the strict majority (i.e. has strictly more votes than each wrong label). (b) Expected token cost for the full self-consistency call (5 samples).

**Solution:**
(a) Let $k$ = number of correct votes (out of 5). Wrong votes split into two labels $W_1,W_2$ each with prob $0.2$ per sample. Let $(k, w_1, w_2)$ be the multinomial counts with $k+w_1+w_2=5$, probabilities $(0.6,0.2,0.2)$.

Correct strictly wins iff $k > w_1$ and $k > w_2$. We sum the multinomial probability over qualifying triples.

Multinomial pmf: $P(k,w_1,w_2) = \dfrac{5!}{k!w_1!w_2!}(0.6)^k(0.2)^{w_1}(0.2)^{w_2}$.

Enumerate triples with $k > w_1$ and $k > w_2$:

| k | (w1,w2) options | coef = 5!/(k!w1!w2!) | $(0.6)^k(0.2)^{w_1+w_2}$ | prob |
|---|---|---|---|---|
| 5 | (0,0) | 1 | $0.6^5 = 0.07776$ | 0.07776 |
| 4 | (1,0),(0,1) | 5 each | $0.6^4\cdot 0.2 = 0.02592$ | $2\cdot 5\cdot 0.02592 = 0.25920$ |
| 3 | (2,0),(0,2),(1,1) | (2,0):10, (0,2):10, (1,1):20 | $0.6^3\cdot 0.2^2 = 0.00864$ | $(10+10+20)\cdot 0.00864 = 40\cdot 0.00864 = 0.34560$ |
| 2 | $w_1<2, w_2<2$ → only (1,1) but then $w_1+w_2=2$ and $k=2$, need $k>w_i$: 2>1 ✓. Coef = $5!/(2!1!1!)=60$? Check: $5!/(2!\,1!\,1!)=120/2=60$ — but $k+w_1+w_2=4\ne 5$. So (2,1,1) has sum 4, invalid.
For $k=2$, $w_1+w_2=3$ → at least one $w_i\ge 2$, so $k>w_i$ fails. None qualify. | — | — | 0 |
| 1,0 | $k\le 1$, need both $w_i<k\le1$, so $w_i=0$, sum=$k\le1<5$. None qualify. | — | — | 0 |

Total = $0.07776 + 0.25920 + 0.34560 = 0.68256$.

(b) Expected cost $= N \times \text{tokens} \times c = 5 \cdot 180 \cdot 2.5\times 10^{-6} = 900 \cdot 2.5\times 10^{-6} = 2.25\times 10^{-3}$ USD $= 0.00225$ USD.

**Answer:** (a) $\boxed{P(\text{correct majority}) \approx 0.6826}$; (b) $\boxed{\$0.00225}$ per query.
