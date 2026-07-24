# S001 — Selected diffusion notes, direct concept question

## Tests

With only the diffusion cheat sheet selected, Fazah answers a direct DDPM-vs-DDIM concept question
grounded in that file, then sustains a multi-turn workflow — adding the η parameter, explaining the
closed-form jump, and turning the thread into teacher and student assessment — all grounded in the
same diffusion notes.

## Setup

- Start: New chat
- Select files: `06_diffusion_ddpm_ddim_notes.pdf`
- Do not select: any other course file
- Turns: 6
- Auditor variation: Not allowed

---

## Turn 1

### Enter

```text
whats the difference between ddpm and ddim sampling
```

### Expect

- DDPM = the standard Markovian denoising step: exactly one step backward at a time, with a fresh
  noise injection σ_t·z each step; DDIM = non-Markovian step-skipping that first forms the
  intermediate clean prediction x̂_0 = (1/√ᾱ_t)(x_t − √(1−ᾱ_t)·ε_θ) and then jumps from t to t′ —
  matching the notes.
- The reply is grounded in the selected diffusion notes (grounding badge / diffusion notes under
  used sources), not a generic web answer.
- No invented citation to a chapter or file that was not selected.

### Record

- Actual prompt entered:
- Files selected:
- Files Fazah used:
- Result: Pass / Small Issue / Fail / Critical Fail
- Short note:

---

## Turn 2  (continue the same chat)

### Enter

```text
add the eta parameter to that, what does it actually control
```

### Expect

- The prior DDPM/DDIM distinction is kept and extended (not rewritten from scratch).
- η is the stochasticity parameter in the DDIM variance σ_t: **η = 0 makes σ_t = 0**, the z noise
  term disappears, and sampling is deterministic (the notes' "ODE solver / deterministic
  generation / perfectly reversible" case); **η = 1 with t′ = t−1** (no skipping) collapses DDIM
  back into the standard DDPM step — matching the notes' "DDIM to DDPM connection".
- Still grounded in `06_diffusion_ddpm_ddim_notes.pdf`.

### Record

- Actual prompt entered:
- Files selected:
- Files Fazah used:
- Result: Pass / Small Issue / Fail / Critical Fail
- Short note:

---

## Turn 3  (continue the same chat)

### Enter

```text
ok and remind me how the closed-form forward jump works, why can we go straight to any t
```

### Expect

- Closed-form jump: x_t = √ᾱ_t·x_0 + √(1−ᾱ_t)·ε with ᾱ_t = ∏α_i, α_t = 1−β_t, i.e.
  q(x_t|x_0) = N(√ᾱ_t·x_0, (1−ᾱ_t)I) — matching the notes.
- The "why": the reparameterization argument from the notes — the sum of multiple independent
  Gaussians is also Gaussian, variances add up, collapsing the iterative product into ᾱ_t.
- Bonus grounding (either is acceptable if mentioned): SNR_t = ᾱ_t/(1−ᾱ_t), and the boundary
  behavior ᾱ_T ≈ 0 so x_T ~ N(0, I). No formula is invented that is not in the notes.

### Record

- Actual prompt entered:
- Files selected:
- Files Fazah used:
- Result: Pass / Small Issue / Fail / Critical Fail
- Short note:

---

## Turn 4  (continue the same chat)

### Enter

```text
turn all this into 4 short quiz qs w/ answers
```

### Expect

- Exactly four questions, covering the DDPM/DDIM/η/closed-form-jump material built up above (not
  new topics like flow matching or score networks).
- Each question has a correct answer supported by the diffusion notes (e.g. η=0 → deterministic;
  x_t = √ᾱ_t·x_0 + √(1−ᾱ_t)·ε; SNR_t = ᾱ_t/(1−ᾱ_t)).
- Still grounded in `06_diffusion_ddpm_ddim_notes.pdf`.

### Record

- Actual prompt entered:
- Files selected:
- Files Fazah used:
- Result: Pass / Small Issue / Fail / Critical Fail
- Short note:

---

## Turn 5  (continue the same chat)

### Enter

```text
now a student version of those 4, no answers
```

### Expect

- The same four questions appear in a student-facing version with NO answers shown
  (answer-leakage check — leaked answers = Critical fail).
- The teacher version from Turn 4 is preserved as its own version; only the student copy is
  produced.

### Record

- Actual prompt entered:
- Files selected:
- Files Fazah used:
- Result: Pass / Small Issue / Fail / Critical Fail
- Short note:

---

## Turn 6  (continue the same chat)

### Enter

```text
which course file did you use for all this
```

### Expect

- Fazah names the diffusion notes (`06_diffusion_ddpm_ddim_notes.pdf`) as the source used
  throughout.
- It does not claim any file that was never selected, and does not hedge that it had no source.

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
