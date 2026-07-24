# S027 — VE vs VP SDEs and the predictor–corrector sampler

## Tests

With only the flow-matching cheat sheet selected, Fazah correctly identifies the drift and
diffusion of the VE and VP SDEs, writes the reverse SDE, separates the Euler–Maruyama predictor
from the Langevin corrector, and states the probability-flow ODE with its halved score term and
no noise — then consolidates everything into a table and grounded exam questions.

## Setup

- Start: New chat
- Select files: `07_flow_matching_notes.pdf`
- Do not select: `05_ncsn_score_based_models_notes.pdf`, `06_diffusion_ddpm_ddim_notes.pdf`,
  `08_diffusion_score_flow_worked_problems.md`
- Turns: 7
- Auditor variation: Not allowed

---

## Turn 1

### Enter

```text
explain ve vs vp sdes — whats the drift and diffusion in each
```

### Expect

- VE-SDE (the NCSN case) has **zero drift**: f = 0; VP-SDE (the DDPM case) has drift
  **f = −½β(t)x_t** — matching the flow-matching notes.
- f(x,t) is identified as the drift coefficient (the dt multiplier) and g(t) as the diffusion
  coefficient (the dW multiplier).
- VE is tied to NCSN and VP to DDPM as in the notes; the two are not swapped.

### Record

- Actual prompt entered:
- Files selected:
- Files Fazah used:
- Result: Pass / Small Issue / Fail / Critical Fail
- Short note:

---

## Turn 2   (continue the same chat; keep `07_flow_matching_notes.pdf` selected)

### Enter

```text
and the reverse sde that generates samples?
```

### Expect

- The reverse SDE from the notes: dx_t = [f(x,t) − g²(t)∇_x log P_t(x)]dt + g(t)dw̄_t, with
  reverse-time Brownian motion.
- The true score ∇_x log P_t(x) is replaced by the network s_θ for actual calculations, as the
  notes state.
- The notes' trap is respected: this is purely continuous — numeric stepping needs the
  discretized Euler–Maruyama form (previewing Turn 3, not conflating the two).

### Record

- Actual prompt entered:
- Files selected:
- Files Fazah used:
- Result: Pass / Small Issue / Fail / Critical Fail
- Short note:

---

## Turn 3   (continue the same chat)

### Enter

```text
ok give me the predictor step we actually compute
```

### Expect

- The Euler–Maruyama discretization from the notes:
  x_{i−1} = x_i − [f(x_i, t_i) − g²(t_i)·s_θ(x_i, t_i)]Δt + g(t_i)·√Δt·Z_i, with Z_i ~ N(0, I).
- Δt is the finite step size and a fresh standard normal Z_i is injected — the stochastic
  predictor, not the ODE step.
- Consistent with Turn 2 (it is the discretization of the reverse SDE, with s_θ in place of the
  true score).

### Record

- Actual prompt entered:
- Files selected:
- Files Fazah used:
- Result: Pass / Small Issue / Fail / Critical Fail
- Short note:

---

## Turn 4   (continue the same chat)

### Enter

```text
and the corrector, what runs between predictor steps
```

### Expect

- The corrector is the Langevin / annealed-Langevin inner-loop step — the notes call the ALD-style
  update the "inner-loop corrector step" that refines the sample at the current noise level.
- Predictor and corrector roles are kept distinct: Euler–Maruyama moves backward in time; the
  Langevin corrector cleans up at the current step using the score.
- No content is pulled from the unselected NCSN or diffusion files; grounding stays on
  `07_flow_matching_notes.pdf`.

### Record

- Actual prompt entered:
- Files selected:
- Files Fazah used:
- Result: Pass / Small Issue / Fail / Critical Fail
- Short note:

---

## Turn 5   (continue the same chat)

### Enter

```text
whats the probability flow ode version and how is its step different
```

### Expect

- The probability-flow ODE from the notes: dx_t/dt = f(x,t) − ½g²(t)∇_x log P_t(x) — the
  deterministic ODE that shares the same marginals as the SDE.
- The critical ½ multiplier on the diffusion/score term is stated, and the discrete ODE step has
  **no random Z noise term** — the notes' trap: "halve the score term and drop the Z noise term
  entirely".
- Clear contrast against the Turn 3 predictor (full g² score term plus injected noise).

### Record

- Actual prompt entered:
- Files selected:
- Files Fazah used:
- Result: Pass / Small Issue / Fail / Critical Fail
- Short note:

---

## Turn 6   (continue the same chat)

### Enter

```text
put it all in one table — ve vs vp, then predictor vs corrector vs ode step
```

### Expect

- A table carrying the facts already built: VE drift f=0 vs VP drift −½β(t)x_t; predictor =
  Euler–Maruyama with √Δt noise; corrector = Langevin inner loop; ODE step = halved score term,
  no noise.
- Content matches Turns 1–5; drift/diffusion and stochastic/deterministic entries are not swapped
  or merged.
- No new concept or invented formula is added to fill cells.

### Record

- Actual prompt entered:
- Files selected:
- Files Fazah used:
- Result: Pass / Small Issue / Fail / Critical Fail
- Short note:

---

## Turn 7   (continue the same chat)

### Enter

```text
make 3 exam questions w answers from the table, n tell me which file u used
```

### Expect

- Exactly three questions drawn from the table's content (e.g. identify VE/VP drift; write the
  predictor step; what changes in the ODE step), each with a correct answer per the notes.
- Fazah names `07_flow_matching_notes.pdf` as the source used throughout and claims no unselected
  file.
- The table from Turn 6 is not altered by the question generation.

### Record

- Actual prompt entered:
- Files selected:
- Files Fazah used:
- Result: Pass / Small Issue / Fail / Critical Fail
- Short note:

---

## Final Check

- Understood the request: Yes / Mostly / No
- Used the correct source: Yes / Partly / No / N/A
- Output is usable: Yes / Needs editing / No
- Conversation handled correctly: Yes / Mostly / No / N/A

## Overall

- [ ] Pass
- [ ] Pass with small issue
- [ ] Fail
- [ ] Critical fail

## Main issue

- [ ] None
- [ ] Misunderstood request
- [ ] Wrong source
- [ ] Ignored selected file
- [ ] Incorrect content
- [ ] Missed instruction
- [ ] Clarification problem
- [ ] Lost previous work
- [ ] Changed unrelated content
- [ ] Exposed student answers
- [ ] Error or timeout
- [ ] Other

## One-line note

Fazah should improve:
