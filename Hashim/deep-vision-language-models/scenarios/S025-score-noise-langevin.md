# S025 — Score ↔ noise and annealed Langevin dynamics, built into assessment

## Tests

With only the NCSN cheat sheet selected, Fazah walks a teacher through the score-based stack in
order — the true score target, the unweighted NCSN loss, the λ(σ)=σ² weighted objective, the
annealed Langevin update, and the DDPM-to-score conversion — then turns the thread into a quiz
plus a clean student version, keeping every formula exactly as the notes state it.

## Setup

- Start: New chat
- Select files: `05_ncsn_score_based_models_notes.pdf`
- Do not select: `04_vae_denoising_autoencoders_notes.pdf`, `06_diffusion_ddpm_ddim_notes.pdf`,
  `08_diffusion_score_flow_worked_problems.md`
- Turns: 8
- Auditor variation: Not allowed

---

## Turn 1

### Enter

```text
what exactly is the target a score network is trained to predict
```

### Expect

- The true score of the Gaussian perturbation: S_true(x̃|x) = −ε/σ, equivalently (x−x̃)/σ² — the
  exact gradient direction pointing back to the clean data, matching the NCSN notes.
- The forward corruption is stated as in the notes: x̃ = x + σε with ε ~ N(0, I).
- Grounded in the selected NCSN cheat sheet, not the VAE or diffusion files (neither is selected).

### Record

- Actual prompt entered:
- Files selected:
- Files Fazah used:
- Result: Pass / Small Issue / Fail / Critical Fail
- Short note:

---

## Turn 2   (continue the same chat; keep `05_ncsn_score_based_models_notes.pdf` selected)

### Enter

```text
ok and whats the unweighted ncsn loss
```

### Expect

- The unweighted denoising score matching loss from the notes: ½‖S_θ(x̃, σ) + ε/σ²‖² — the basic
  squared Euclidean distance between the network's prediction and the true score target.
- Matches Turn 1: the target inside the loss is the same −ε/σ² / true-score quantity, not a new
  invented target.
- Reflects the notes' trap warning: with no λ or weighting mentioned, this basic Euclidean form is
  the default.

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
what changes when we add the sigma squared weighting
```

### Expect

- The weighted NCSN objective with λ(σ) = σ²: L(θ) = ‖σ·S_θ(x̃, σ) + ε‖² — the network's
  prediction is multiplied by σ before adding ε and squaring, as the notes' trap warning says.
- λ(σ) = σ² is named as the professor's weighting factor that balances the loss across noise
  levels.
- The unweighted loss from Turn 2 is not overwritten or contradicted; the two forms are kept
  distinct.

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
now sampling — walk me through one step of annealed langevin dynamics
```

### Expect

- The ALD update rule as in the notes: x ← x + (α/2)·s_θ(x, σ) + √α·z, with z a fresh N(0, I)
  noise vector drawn for that specific step.
- The notes' trap is respected: the step size is divided by 2 on the gradient/score term, but the
  noise term uses the square root of the step size.
- Bonus grounding (acceptable if mentioned): the step size schedule α_i = ε_step·σ_i²/σ_L² from
  the notes. Nothing is invented beyond the cheat sheet.

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
if i have a ddpm network that predicts noise, how do i get the score out of it
```

### Expect

- The DDPM-to-NCSN conversion from the notes: S_θ(x_t, t) = −ε_θ(x_t, t)/√(1−ᾱ_t).
- The sign is negative and the denominator is √(1−ᾱ_t) (not σ or √ᾱ_t) — a swapped or garbled
  formula is a fail.
- Still grounded in the selected NCSN cheat sheet; no DDPM sampling content is pulled from the
  unselected diffusion notes.

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
turn all this into 5 quiz questions w answers
```

### Expect

- Exactly five questions, covering the material built up in Turns 1–5 (true score, unweighted
  loss, λ(σ)=σ² weighting, ALD update, DDPM→score conversion), not new topics like flow matching.
- Each answer is supported by the NCSN notes (e.g. true score = −ε/σ ≡ (x−x̃)/σ²; ALD step
  x + (α/2)s_θ + √α·z; conversion −ε_θ/√(1−ᾱ_t)).
- Still grounded in `05_ncsn_score_based_models_notes.pdf`.

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
now a student version, no answers
```

### Expect

- The same five questions in a student-facing copy with NO answers shown (answer-leakage check —
  leaked answers = Critical fail).
- Question count and topics are unchanged; only the answers are removed.
- The teacher version from Turn 6 is preserved as its own version.

### Record

- Actual prompt entered:
- Files selected:
- Files Fazah used:
- Result: Pass / Small Issue / Fail / Critical Fail
- Short note:

---

## Turn 8   (continue the same chat)

### Enter

```text
which course file did u use for all this
```

### Expect

- Fazah names the NCSN cheat sheet (`05_ncsn_score_based_models_notes.pdf`) as the source used
  throughout.
- It does not claim the VAE, diffusion, or worked-problems files, none of which were selected.
- The answer is consistent with the used-sources shown across the conversation.

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
