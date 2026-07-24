# S006 — Source changes during the conversation

## Tests

Fazah starts a thread grounded in the VAE notes, then the teacher switches the selection to the
diffusion notes mid-chat. Fazah must ground each turn in the currently right file, resolve "the
first file" / "the second file" references correctly after the switch, and build a quiz that draws
on both without mixing up attribution.

## Setup

- Start: New chat
- Select files: `04_vae_denoising_autoencoders_notes.pdf` (switched to
  `06_diffusion_ddpm_ddim_notes.pdf` before Turn 3)
- Do not select: any other course file
- Turns: 8
- Auditor variation: Not allowed

---

## Turn 1  (VAE notes selected)

### Enter

```text
explain tweedies formula from the selected notes
```

### Expect

- Tweedie's formula: E[x|x̃] = x̃ + σ²∇log P(x̃) — maps a noisy image back toward the clean data
  manifold using the score, with the notes' intuition (x̃ is where you are, ∇log P(x̃) points toward
  clean images, σ² is the step size).
- Grounded in the selected VAE notes; context of the DAE forward corruption x̃ = x + ε,
  ε ~ N(0, σ²I) is consistent with the file.
- No invented citation to a file that was not selected.

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
and the reparameterization trick, why do we need it
```

### Expect

- z = μ_φ(x) + σ_φ(x)⊙ε with ε ~ N(0, I) — matching the VAE notes.
- The "why": it decouples the random sampling from the network's deterministic parameters so
  backpropagation can occur.
- Still grounded in `04_vae_denoising_autoencoders_notes.pdf`.

### Record

- Actual prompt entered:
- Files selected:
- Files Fazah used:
- Result: Pass / Small Issue / Fail / Critical Fail
- Short note:

---

## Turn 3  (before entering: deselect the VAE notes, select `06_diffusion_ddpm_ddim_notes.pdf`; continue the same chat)

### Enter

```text
ok switching to the diffusion notes now — whats the closed-form forward jump
```

### Expect

- Fazah switches sources cleanly: x_t = √ᾱ_t·x_0 + √(1−ᾱ_t)·ε with ᾱ_t = ∏α_i, α_t = 1−β_t,
  i.e. q(x_t|x_0) = N(√ᾱ_t·x_0, (1−ᾱ_t)I) — from the diffusion notes.
- Used sources now reflect `06_diffusion_ddpm_ddim_notes.pdf`, not the VAE notes.
- It does not re-ask what the teacher wants; the topic switch is handled in stride.

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
the second file uses basically the same gaussian trick as the first one right?
```

### Expect

- Reference resolution: "the second file" = the diffusion notes, "the first one" = the VAE notes
  (asking which file is meant = Small Issue; resolving them backwards = Fail).
- The link is real and stated per the notes: the diffusion notes justify the closed-form jump via
  the reparameterization argument (sum of independent Gaussians is Gaussian, variances add), the
  same trick as the VAE's z = μ_φ + σ_φ⊙ε sampling layer.
- Neither file's content is misattributed to the other.

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
whats the snr formula in the second file
```

### Expect

- SNR_t = ᾱ_t/(1−ᾱ_t) — from the diffusion notes ("ratio of data to noise").
- The answer comes from `06_diffusion_ddpm_ddim_notes.pdf`; no SNR formula is invented for or
  attributed to the VAE notes.

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
one more from the first file — whats in the elbo, the two pieces
```

### Expect

- "The first file" resolves back to the VAE notes: the negative ELBO = reconstruction term
  −E_q[log P_θ(x|z)] plus the KL divergence penalty D_KL(q_φ(z|x) || P_θ(z)) — matching the notes'
  Master ELBO objective.
- Fazah answers from the VAE notes' content even though the current selection changed (an honest
  note that it is recalling the earlier file is fine); it does not attribute the ELBO to the
  diffusion notes.

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
make 4 quiz questions w/ answers, 2 from each file, label which file each is from
```

### Expect

- Exactly four questions: two labeled to `04_vae_denoising_autoencoders_notes.pdf` (Tweedie,
  reparameterization, or ELBO) and two labeled to `06_diffusion_ddpm_ddim_notes.pdf` (closed-form
  jump, SNR, or the shared-Gaussian-trick link).
- Every label is correct — a VAE fact labeled as the diffusion file (or vice versa) = Fail on
  wrong source.
- Answers are supported by the respective notes.

### Record

- Actual prompt entered:
- Files selected:
- Files Fazah used:
- Result: Pass / Small Issue / Fail / Critical Fail
- Short note:

---

## Turn 8  (continue the same chat)

### Enter

```text
now the student version, no answers and no file labels
```

### Expect

- The same four questions with NO answers and no source labels shown
  (answer-leakage check — leaked answers = Critical fail).
- The teacher version from Turn 7 is preserved as its own version; question wording is unchanged.

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
