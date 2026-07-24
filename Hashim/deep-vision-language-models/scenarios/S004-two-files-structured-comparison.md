# S004 — Two files selected for a structured NCSN vs DDPM comparison

## Tests

With the NCSN and diffusion cheat sheets both selected, Fazah synthesizes a correct NCSN-vs-DDPM
comparison across corruption, training target, and sampling, attributes each side to the right
file, then iterates on a comparison table and turns it into assessment.

## Setup

- Start: New chat
- Select files: `05_ncsn_score_based_models_notes.pdf`, `06_diffusion_ddpm_ddim_notes.pdf`
- Do not select: any other course file
- Turns: 7
- Auditor variation: Not allowed

---

## Turn 1

### Enter

```text
compare how ncsn and ddpm corrupt the data in the forward process
```

### Expect

- NCSN: x̃ = x + σε — noise is added at a given level σ with **no scaling of the signal** (from the
  NCSN notes).
- DDPM: Markovian iterative step scaling by √(1−β_t), with the closed-form jump
  x_t = √ᾱ_t·x_0 + √(1−ᾱ_t)·ε — the signal is **shrunk** by √ᾱ_t as noise is added (from the
  diffusion notes).
- Used sources reflect both selected files; each side of the comparison is attributed to the right
  one, with no third file cited.

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
and what does each one train the network to predict
```

### Expect

- NCSN: the network predicts the **score**; the ground-truth target is the true Gaussian score
  S_true(x̃|x) = −ε/σ (equivalently (x−x̃)/σ²) — matching the NCSN notes.
- DDPM: the network predicts the **noise ε**, trained with the simplified MSE objective
  L_simple(θ) = ||ε − ε_θ||² — matching the diffusion notes.
- The Turn 1 comparison is extended, not rewritten from scratch.

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
now sampling — annealed langevin vs the ddpm step
```

### Expect

- NCSN: annealed Langevin dynamics update x̃_t = x̃_{t−1} + (α_i/2)·s_θ(x̃_{t−1}, σ_i) + √α_i·Z_t,
  with step size α_i = ε_step·σ_i²/σ_L² — including the notes' trap: **halve the step size for the
  gradient term, square-root it for the noise term**.
- DDPM: one-step denoising x_{t−1} = (1/√α_t)(x_t − ((1−α_t)/√(1−ᾱ_t))·ε_θ) + σ_t·z, with z = 0 at
  the final t=1 step — matching the diffusion notes.
- Each sampler is attributed to its own file.

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
theres a conversion between the two right? noise prediction to score
```

### Expect

- The DDPM-to-NCSN score conversion from the NCSN notes:
  S_θ(x_t, t) = −ε_θ(x_t, t)/√(1−ᾱ_t).
- Correct direction and sign; no invented alternative formula.
- Grounded in the selected files (the conversion lives in
  `05_ncsn_score_based_models_notes.pdf`).

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
great, put all of that into one comparison table, ncsn column vs ddpm column
```

### Expect

- A two-column table reusing the corruption / training-target / sampling / conversion material
  built in Turns 1–4 (not new material).
- No cell contradicts the notes (e.g. score target stays −ε/σ; DDPM target stays ε).
- Still grounded in both selected files.

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
add a row for the loss functions, dont touch the rest of the table
```

### Expect

- One new row: NCSN unweighted denoising score-matching loss (and/or the weighted objective with
  λ(σ) = σ²) vs the DDPM simplified loss ||ε − ε_θ||².
- The rest of the table is preserved unchanged (selective edit — rewriting other rows = Fail on
  lost previous work).

### Record

- Actual prompt entered:
- Files selected:
- Files Fazah used:
- Result: Pass / Small Issue / Fail / Critical Fail
- Short note:

---

## Turn 7  (continue the same chat)

### Enter

```text
turn the table into a 6 question quiz w/ answer key
```

### Expect

- Exactly six questions derived from the table's rows (corruption, targets, sampling, conversion,
  losses), each with a correct answer supported by the two selected files.
- No question drifts into unselected material (flow matching, VAEs, alignment).
- Used sources still reflect only the two selected files.

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
