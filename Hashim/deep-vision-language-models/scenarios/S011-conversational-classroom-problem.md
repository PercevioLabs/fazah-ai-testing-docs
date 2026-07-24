# S011 — Conversational classroom problem

## Tests

Fazah turns a conversational classroom complaint — students conflating score matching with plain
denoising — into a correct pedagogical build-out grounded in the NCSN notes: the distinguishing
formula, the multiple-noise-level story, a board plan, an activity, and exit tickets.

## Setup

- Start: New chat
- Select files: none
- Do not select: n/a
- Turns: 7
- Auditor variation: Not allowed

---

## Turn 1

### Enter

```text
half my class thinks score matching is just denoising, how do i untangle that in one lecture
```

### Expect

- Recognizes this as a teaching problem about score-based models, grounded in the NCSN notes
  (`05_ncsn_score_based_models_notes.pdf`), not a request to merely define denoising.
- Draws the correct distinction: a plain denoiser predicts the clean image (MSE reconstruction),
  while a score network predicts the score — the gradient direction back to the data, whose true
  target for Gaussian noise is S_true(x̃|x) = −ε/σ (equivalently (x−x̃)/σ²).
- Offers a concrete lecture-level approach (not just a definition dump).

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
ok whats the one formula i can put on the board that makes the difference obvious
```

### Expect

- Gives the true Gaussian score from the notes: S_true(x̃|x) = −ε/σ = (x−x̃)/σ² — the target the
  score network predicts, which is a direction/gradient, not a reconstructed image.
- Explains the contrast in one line: the denoiser's target is x itself; the score model's target
  is −ε/σ.
- No invented formula outside the notes.

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
and how do i explain why we need multiple noise levels, they always ask that
```

### Expect

- Explains the NCSN multi-noise-level design consistently with the notes: the network is
  noise-conditional S_θ(x̃, σ), the objective is balanced across levels with the weighting
  λ(σ) = σ², and sampling anneals through the schedule of σ_i levels.
- Connects it to annealed Langevin dynamics: step size α_i = ε_step·σ_i²/σ_L² shrinks as the
  noise level anneals toward the smallest level σ_L.
- Stays on the same score-matching thread; no topic switch.

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
gimme a board plan for the lecture, like 4 sections
```

### Expect

- Produces exactly four lecture sections covering the material built up above — e.g. corruption
  x̃ = x + σε, the true score target −ε/σ vs the denoiser's target, the NCSN loss (unweighted and
  λ(σ)=σ² weighted), and annealed Langevin sampling
  x̃_t = x̃_{t−1} + (α_i/2)·S_θ(x̃_{t−1}, σ_i) + √α_i·Z_t.
- Every section is grounded in the NCSN notes; nothing off-corpus is introduced.
- The plan visibly targets the misconception (score ≠ plain denoising) rather than being a generic
  score-matching lecture.

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
add a quick misconception check the students can do in pairs
```

### Expect

- Adds one short pair activity that directly probes the misconception (e.g. classify targets as
  "clean image" vs "score vector", or compute −ε/σ for a small example).
- The activity's correct answers are checkable against the notes (true score = −ε/σ).
- The four board-plan sections from turn 4 are preserved, not rewritten.

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
make 3 exit ticket questions on this
```

### Expect

- Produces exactly three exit-ticket questions drawn only from the lecture content above (true
  score, noise levels / λ(σ)=σ², annealed Langevin).
- Each has a correct answer supported by the NCSN notes.
- No new topics (DDPM, flow matching, VAEs) sneak in.

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
which notes should i tell them to read for this
```

### Expect

- Points to the NCSN notes (`05_ncsn_score_based_models_notes.pdf`) as the reading for this
  lecture.
- Does not invent a different or non-existent source (mentioning the VAE notes' Tweedie bridge as
  optional extra reading is acceptable, but the NCSN notes must be primary).

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
