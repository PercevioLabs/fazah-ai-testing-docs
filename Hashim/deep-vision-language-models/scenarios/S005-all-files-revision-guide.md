# S005 — All files selected, revision guide built out across many turns

## Tests

With every course file selected, Fazah builds a topic-organized revision guide for the open-book
final, then sustains a long workflow — cross-file connections, added formulas, a condensed version,
a cumulative quiz with teacher and student versions, and a glossary — preserving prior work at each
step and grounding every section in the right file.

## Setup

- Start: New chat
- Select files: all thirteen course files (`AI623_course_outline.pdf`, `01_dvlm_introduction.pptx`,
  `04_vae_denoising_autoencoders_notes.pdf`, `05_ncsn_score_based_models_notes.pdf`,
  `06_diffusion_ddpm_ddim_notes.pdf`, `07_flow_matching_notes.pdf`,
  `08_diffusion_score_flow_worked_problems.md`, `09_ar_alignment_rlhf_notes.pdf`,
  `10_ar_alignment_worked_problems.md`, `11_ppo_dpo_grpo_alignment.pptx`,
  `12_vlm_vit_clip_reasoning.md`, `13_exam_master_cheatsheet.md`,
  `14_handwritten_class_notes_L2.pdf`)
- Do not select: n/a
- Turns: 9
- Auditor variation: Not allowed

---

## Turn 1

### Enter

```text
make a concise revision guide for this course for the open-book final, organized by topic
```

### Expect

- Organized by the course's topic blocks, each grounded in the right file(s): intro definitions
  (LLM vs VLM vs MLLM); VAEs (Tweedie, reparameterization, ELBO); NCSN (true score −ε/σ, annealed
  Langevin); diffusion (closed-form jump, SNR_t = ᾱ_t/(1−ᾱ_t), DDPM vs DDIM η); flow matching
  (VE/VP SDEs, v = x_1 − x_0); AR + alignment (softmax temperature, RLHF/PPO/DPO/GRPO); VLM (ViT
  196 patches/197 tokens, CLIP contrastive loss).
- No content is attributed to `14_handwritten_class_notes_L2.pdf` (it has no extractable text —
  invented content from it = Critical fail); at most an honest note that it could not be used.
- Used sources reflect the breadth of the selected files, not just one.

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
add 5 cross-topic connections, dont rewrite the guide
```

### Expect

- Exactly five cross-file connections added; the Turn 1 guide is preserved (selective expansion).
- Connections are real per the content map, e.g.: DDPM noise ↔ NCSN score conversion
  S_θ = −ε_θ/√(1−ᾱ_t) (05 ↔ 06); VE-SDE = NCSN and VP-SDE = DDPM in continuous time (05/06 ↔ 07);
  Tweedie's formula as the score-based denoising bridge (04 ↔ 05); DDIM η=0 determinism ↔ the
  probability-flow ODE (06 ↔ 07); the reparameterization/sum-of-Gaussians trick behind both the
  VAE latent and the DDPM closed-form jump (04 ↔ 06); softmax temperature in AR sampling ↔ CLIP's
  temperature-scaled logits (09 ↔ 12).
- No connection is fabricated between files that do not share the claimed content.

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
now add 2 key formulas to each topic section
```

### Expect

- Two formulas per topic section, each grounded in that section's file (e.g. VAE:
  E[x|x̃] = x̃ + σ²∇log P(x̃) and z = μ_φ(x) + σ_φ(x)⊙ε; NCSN: S_true = −ε/σ and the Langevin
  update; diffusion: x_t = √ᾱ_t·x_0 + √(1−ᾱ_t)·ε and SNR_t = ᾱ_t/(1−ᾱ_t); flow matching:
  x_t = t·x_1 + (1−t)·x_0 and v = x_1 − x_0; alignment: the Bradley–Terry loss and the GRPO
  normalized advantage; VLM: N = HW/P² and the CLIP symmetric loss).
- Formulas are transcribed faithfully — wrong signs or swapped terms = Incorrect content.
- The existing guide and the five connections from Turns 1–2 are preserved.

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
ok make a one-page condensed version
```

### Expect

- A single-page condensation of the built-up guide, keeping every topic section.
- Substance is condensed, not replaced with new topics; formulas that survive stay correct.

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
now a 10-question cumulative quiz spanning the whole course
```

### Expect

- Exactly ten questions, collectively spanning the topic blocks (not concentrated on one file).
- Each question is grounded in course material and checkable against the notes (e.g. η=0
  deterministic DDIM; VE-SDE zero drift; PPO needs policy + reference + reward + critic while GRPO
  drops the critic; ViT 224×224 with P=16 → 196 patches, 197 tokens).
- Used sources span multiple files; nothing is drawn from the unreadable handwritten file.

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
gimme the teacher answer key for that quiz
```

### Expect

- An answer key for the same ten questions from Turn 5 (same questions, now with answers).
- Answers are supported by the notes; the question set is unchanged.

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
now a student version of the quiz, no answers
```

### Expect

- The same ten questions in a student-facing version with NO answers shown
  (answer-leakage check — leaked answers = Critical fail).
- The teacher key from Turn 6 is preserved as its own version.

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
add a glossary to the revision guide
```

### Expect

- A glossary of course terms drawn from the selected files (e.g. score, ELBO, reparameterization,
  SNR, η, drift/diffusion coefficients, nucleus sampling, advantage, [CLS] token, InfoNCE) is
  added to the guide.
- Definitions match the notes; the guide, connections, formulas, and quizzes built earlier are
  preserved.

### Record

- Actual prompt entered:
- Files selected:
- Files Fazah used:
- Result: Pass / Small Issue / Fail / Critical Fail
- Short note:

---

## Turn 9  (continue the same chat)

### Enter

```text
summarize what we built n which files fed each section
```

### Expect

- An inventory of the artifacts actually produced (guide, connections, formulas, condensed
  version, quiz, teacher key, student version, glossary) — no fabricated extras.
- Each section is attributed to the correct file(s); no source is invented, and the handwritten
  file is not credited with content.

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
