# S003 — Wrong file selected for the topic (conflict, then recovery)

## Tests

When the selected VAE notes do not support the requested GRPO topic, Fazah honestly flags the gap
instead of fabricating content, then — across a sustained workflow — recovers onto the alignment
notes and builds the full PPO/DPO/GRPO lesson and assessment from them.

## Setup

- Start: New chat
- Select files: `04_vae_denoising_autoencoders_notes.pdf` only
- Do not select: `09_ar_alignment_rlhf_notes.pdf` (the correct source — auditor withholds it until
  Turn 3)
- Turns: 8
- Auditor variation: Not allowed

---

## Turn 1  (VAE notes selected)

### Enter

```text
explain grpo from the selected notes
```

### Expect

- Fazah recognizes the selected VAE notes do NOT cover GRPO (they cover DAEs, Tweedie's formula,
  reparameterization, ELBO — no RL alignment) and says so honestly (one-line gap note), rather
  than blocking.
- It offers/asks to use the alignment material, or proceeds only with a clear caveat that the
  content is not from the selected file.
- It does NOT fabricate GRPO content attributed to the VAE notes. (Fabricated GRPO content claimed
  to be from `04_vae_denoising_autoencoders_notes.pdf` = Critical fail.)

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
hmm ok so which file should i use for grpo then
```

### Expect

- Fazah points to the alignment material (`09_ar_alignment_rlhf_notes.pdf`, and/or the PA2 deck
  `11_ppo_dpo_grpo_alignment.pptx`) as the right source for GRPO.
- It does not invent a filename; it references actual course files.

### Record

- Actual prompt entered:
- Files selected:
- Files Fazah used:
- Result: Pass / Small Issue / Fail / Critical Fail
- Short note:

---

## Turn 3  (before entering: select `09_ar_alignment_rlhf_notes.pdf`; continue the same chat)

### Enter

```text
ok use these alignment notes instead
```

### Expect

- Fazah switches to the alignment notes; used sources now reflect
  `09_ar_alignment_rlhf_notes.pdf`.
- It confirms the source change without re-asking what the topic is (the goal is unchanged: GRPO).

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
now explain grpo properly from it
```

### Expect

- GRPO computes advantage **without a value model**: sample K completions, take their mean reward
  r̄ and standard deviation σ_r, and normalize — Ã_{i,t} = (r_i − r̄)/σ_r — matching the notes'
  "GRPO Relative Advantage (Normalization)".
- Grounded in the alignment notes, not the VAE notes.
- No GRPO mechanics are invented beyond the notes (e.g. no fabricated clipping constants).

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
how does that differ from ppo and dpo
```

### Expect

- PPO: probability ratio ρ = π_θ/π_θold, clipped surrogate loss min(ρA, clip(ρ, 1−ε, 1+ε)A), and
  KL-penalized reward shaping β·log(π_θ/π_ref) against the reference model — matching the notes.
- DPO: bypasses the reward model, directly widening the gap between the preferred and rejected
  responses via the implicit reward margin β·log(π_θ(y+)/π_ref(y+)) vs β·log(π_θ(y−)/π_ref(y−));
  the reward model itself is trained with the Bradley–Terry pairwise loss
  −log σ(r_ψ(x,y+) − r_ψ(x,y−)).
- The distinguishing point stays correct: GRPO's difference is advantage from group statistics
  (no value model/critic); DPO's is no separate reward model. Still grounded in
  `09_ar_alignment_rlhf_notes.pdf`.

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
put ppo vs dpo vs grpo into a comparison table
```

### Expect

- A table contrasting the three, reusing the definitions and formulas built above (not new
  material).
- Still grounded in the alignment notes; each row is checkable against them.

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
make 5 questions from that table for students, no answers shown
```

### Expect

- Exactly five questions derived from the comparison table.
- Student-facing version with NO answers shown (answer-leakage check — leaked answers = Critical
  fail).

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
confirm the source, which file did these questions come from
```

### Expect

- Fazah names the alignment notes (`09_ar_alignment_rlhf_notes.pdf`), not the VAE notes.
- It does not credit the original (wrong) VAE selection for the GRPO/PPO/DPO content.

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
