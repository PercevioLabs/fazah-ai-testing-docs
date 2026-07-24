# S024 — DAE, Tweedie, and the reparameterization trick

## Tests

With only the VAE notes selected, Fazah works through three core results in sequence — the DAE
forward corruption, Tweedie's formula, and the reparameterization trick including WHY it exists
(backprop through sampling) — then assembles them into a student summary sheet that ends with
self-check questions, keeping every formula exactly as the notes state it.

## Setup

- Start: New chat
- Select files: `04_vae_denoising_autoencoders_notes.pdf`
- Do not select: any other file
- Turns: 7
- Auditor variation: Not allowed

---

## Turn 1

### Enter

```text
explain how a denoising autoencoder corrupts its input
```

### Expect

- Gives the notes' forward corruption: x̃ = x + ε with ε sampled from N(0, σ²I) — Gaussian noise
  added to the clean image.
- Includes the notes' intuition: the noise pushes the clean image off the data manifold.
- Grounded in the selected VAE notes; no other corruption schemes invented.

### Record

- Actual prompt entered:
- Files selected:
- Files Fazah used:
- Result: Pass / Small Issue / Fail / Critical Fail
- Short note:

---

## Turn 2   (continue the same chat; keep `04_vae_denoising_autoencoders_notes.pdf` selected)

### Enter

```text
ok now whats tweedie's formula and what does it actually do
```

### Expect

- States Tweedie's formula as in the notes: E[x|x̃] = x̃ + σ²∇log P(x̃).
- Explains what it does: uses the score vector (gradient of the log-density) to map a noisy
  image back to the clean data manifold — the posterior mean of the clean data.
- Reflects the notes' intuition (x̃ is where you are, ∇log P(x̃) is the direction of the clean
  images, σ² is how big a step you take); no invented variants of the formula.

### Record

- Actual prompt entered:
- Files selected:
- Files Fazah used:
- Result: Pass / Small Issue / Fail / Critical Fail
- Short note:

---

## Turn 3   (continue the same chat; keep `04_vae_denoising_autoencoders_notes.pdf` selected)

### Enter

```text
now the reparameterization trick, write the formula out
```

### Expect

- Writes the trick exactly as the notes have it: z = μ_φ(x) + σ_φ(x)⊙ε with ε∼N(0, I).
- Identifies the pieces correctly: μ_φ, σ_φ are the encoder's deterministic outputs; ε is the
  random sample.
- No mixing in of the DAE corruption or other formulas from earlier turns.

### Record

- Actual prompt entered:
- Files selected:
- Files Fazah used:
- Result: Pass / Small Issue / Fail / Critical Fail
- Short note:

---

## Turn 4   (continue the same chat; keep `04_vae_denoising_autoencoders_notes.pdf` selected)

### Enter

```text
but why do we even need that trick
```

### Expect

- Gives the notes' reason: it decouples the random sampling (ε∼N(0, I)) from the network's
  deterministic parameters (μ_φ, σ_φ) so backpropagation can occur — gradients can flow to the
  encoder through what would otherwise be a non-differentiable sampling step.
- Ties the answer to the formula from Turn 3 rather than restating it in the abstract.
- Does not drift into unrelated VAE material (ELBO, posterior collapse) unless briefly as
  context.

### Record

- Actual prompt entered:
- Files selected:
- Files Fazah used:
- Result: Pass / Small Issue / Fail / Critical Fail
- Short note:

---

## Turn 5   (continue the same chat; keep `04_vae_denoising_autoencoders_notes.pdf` selected)

### Enter

```text
put all 3 into one summary sheet i can hand my students
```

### Expect

- One sheet covering all three items with the formulas carried over exactly: DAE corruption
  x̃ = x + ε, ε∼N(0, σ²I); Tweedie E[x|x̃] = x̃ + σ²∇log P(x̃); reparameterization
  z = μ_φ(x) + σ_φ(x)⊙ε — plus the why-backprop reason from Turn 4.
- Nothing from Turns 1–4 is dropped or silently reworded into a wrong meaning.
- Student-appropriate framing; still grounded only in the VAE notes.

### Record

- Actual prompt entered:
- Files selected:
- Files Fazah used:
- Result: Pass / Small Issue / Fail / Critical Fail
- Short note:

---

## Turn 6   (continue the same chat; keep `04_vae_denoising_autoencoders_notes.pdf` selected)

### Enter

```text
end the sheet with 4 self-check questions students can answer from it
```

### Expect

- Exactly four self-check questions appended to the sheet, each answerable from the sheet's own
  content (e.g. write the corruption step; state Tweedie's formula; compute/write z given μ, σ,
  ε; say why the trick is needed).
- The rest of the sheet (formulas and explanations) is unchanged.
- Questions stay within the three concepts; no new material smuggled in.

### Record

- Actual prompt entered:
- Files selected:
- Files Fazah used:
- Result: Pass / Small Issue / Fail / Critical Fail
- Short note:

---

## Turn 7   (continue the same chat; keep `04_vae_denoising_autoencoders_notes.pdf` selected)

### Enter

```text
make sure the self-check qs dont have answers printed next to them, this goes straight to students
```

### Expect

- Confirms/produces the student-facing sheet with the four self-check questions and NO printed
  answers next to them (the reference formulas earlier in the sheet may remain — they are the
  study material).
- No separate answer key leaks into the student sheet (leakage = Critical fail).
- Still four questions; sheet content otherwise unchanged.

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
