# S040 — Complete course package across a long conversation

## Tests

Over sixteen turns Fazah holds long-range context across three files (intro, diffusion,
AR/alignment), produces many connected artifacts — revision summary, cumulative quiz, student notes,
lesson outline — with correct audiences, keeps every edit selective, preserves the intro deck's exact
definitions everywhere, verifies quiz coverage, and ends with an accurate inventory of every artifact,
its audience, and its source.

## Setup

- Start: New chat
- Select files: `01_dvlm_introduction.pptx` + `06_diffusion_ddpm_ddim_notes.pdf` + `09_ar_alignment_rlhf_notes.pdf`
- Do not select: `04_vae_denoising_autoencoders_notes.pdf`, `12_vlm_vit_clip_reasoning.md`, `13_exam_master_cheatsheet.md`
- Turns: 16
- Auditor variation: Allowed — see the Auditor variation section

---

## Turn 1

### Enter

```text
can u make a revision summary that connects these 3 files for my students
```

### Expect

- A revision summary connecting the intro (LLM/VLM/MLLM, course scope), diffusion (DDPM/DDIM),
  and AR/alignment (chain rule, softmax, RLHF) material.
- Grounded across all three selected files, with used sources listing all three.
- No content from unselected files (VAE, VLM notes, master cheat sheet).

### Record

- Actual prompt entered:
- Files selected:
- Files Fazah used:
- Result: Pass / Small Issue / Fail / Critical Fail
- Short note:

---

## Turn 2   (continue the same chat)

### Enter

```text
keep the llm vlm mllm definitions word for word from the intro deck
```

### Expect

- The three definitions match the deck exactly: LLM = large model primarily trained on language,
  understands and generates text; VLM = an LLM with a vision encoder, understands language and
  images, generates text; MLLM = processes, understands and generates text, images, video, audio.
- Only the definitions section changes; the rest of the summary is preserved.

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
add the key diffusion formulas to the summary
```

### Expect

- Key formulas from the diffusion notes are added (e.g. ᾱ_t = ∏α_i, closed-form jump
  x_t = √ᾱ_t·x_0 + √(1−ᾱ_t)·ε, SNR_t = ᾱ_t/(1−ᾱ_t), DDIM η behavior).
- Formulas are faithful to the notes, not invented variants.
- Prior summary content (including the exact definitions) is preserved.

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
same for the AR and alignment side
```

### Expect

- Key AR/alignment items are added from the AR notes (autoregressive chain rule
  P_θ(x)=∏P_θ(x_t|x_<t), softmax with temperature, cross-entropy / perplexity, RLHF objective
  with KL penalty, DPO / GRPO).
- Grounded in `09_ar_alignment_rlhf_notes.pdf`, not the unselected PA2 deck or worked problems.
- Earlier sections unchanged.

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
now a 10 question cumulative quiz across all 3 files
```

### Expect

- Exactly ten questions spanning the three files (intro definitions/scope, diffusion, AR/alignment).
- Grounded; no content pulled from unselected files.
- Consistent with the revision summary's coverage.

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
teacher answer key pls
```

### Expect

- A teacher answer key for the ten questions, consistent with Turn 5's quiz.
- Answers are correct per the notes (e.g. VLM generates text; η=0 makes DDIM deterministic;
  perplexity = e^loss).

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
make short student notes covering the same ground
```

### Expect

- Short student-facing notes across the three files, consistent with the revision summary.
- The exact LLM/VLM/MLLM definitions are used, not paraphrased.
- No quiz answers leak into the notes (answer-leakage check — leaked answers = Critical fail).

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
what have we made so far, whos each thing for
```

### Expect

- An accurate mid-conversation inventory: revision summary (+ formulas), quiz, teacher key,
  student notes.
- Each artifact is labelled with its audience (student or teacher).
- Sources correctly given as the three selected files; no fabricated artifacts.

### Record

- Actual prompt entered:
- Files selected:
- Files Fazah used:
- Result: Pass / Small Issue / Fail / Critical Fail
- Short note:

---

## Turn 9   (continue the same chat)

### Enter

```text
add a glossary to the student notes
```

### Expect

- A glossary of key terms grounded in the three files (e.g. LLM/VLM/MLLM, noise schedule ᾱ_t,
  SNR, DDIM, perplexity, RLHF, KL penalty).
- Definitions consistent with the sources; no invented terms.
- The rest of the student notes is preserved.

### Record

- Actual prompt entered:
- Files selected:
- Files Fazah used:
- Result: Pass / Small Issue / Fail / Critical Fail
- Short note:

---

## Turn 10   (continue the same chat)

### Enter

```text
now a lesson outline for one 180 min revision session using all this
```

### Expect

- A teacher-facing outline for a single 180-minute revision session covering the three topic
  blocks (intro/definitions, diffusion, AR/alignment).
- It references the artifacts already made (summary, quiz, notes) rather than inventing new ones.
- Grounded in the same three files.

### Record

- Actual prompt entered:
- Files selected:
- Files Fazah used:
- Result: Pass / Small Issue / Fail / Critical Fail
- Short note:

---

## Turn 11   (continue the same chat)

### Enter

```text
put timings on the outline
```

### Expect

- Each outline block gets a time allocation summing to 180 minutes.
- The outline's content and the other artifacts are unchanged.

### Record

- Actual prompt entered:
- Files selected:
- Files Fazah used:
- Result: Pass / Small Issue / Fail / Critical Fail
- Short note:

---

## Turn 12   (continue the same chat)

### Enter

```text
add one discussion question per topic block
```

### Expect

- Exactly three discussion questions (one per block: intro, diffusion, AR/alignment), each tied
  to that block's material.
- Prior outline content and timings are preserved.

### Record

- Actual prompt entered:
- Files selected:
- Files Fazah used:
- Result: Pass / Small Issue / Fail / Critical Fail
- Short note:

---

## Turn 13   (continue the same chat)

### Enter

```text
quiz student version, no answers
```

### Expect

- A student version of the ten-question quiz with NO answers shown (answer-leakage check —
  leaked answers = Critical fail).
- The teacher key from Turn 6 is not overwritten.
- Question wording matches the current quiz.

### Record

- Actual prompt entered:
- Files selected:
- Files Fazah used:
- Result: Pass / Small Issue / Fail / Critical Fail
- Short note:

---

## Turn 14   (continue the same chat)

### Enter

```text
does the quiz actually cover all 3 files? check it
```

### Expect

- Fazah confirms the ten questions draw on all three files (intro, diffusion, AR/alignment).
- If a file is under- or over-represented, it notes this and rebalances.
- No question traces to an unselected file.

### Record

- Actual prompt entered:
- Files selected:
- Files Fazah used:
- Result: Pass / Small Issue / Fail / Critical Fail
- Short note:

---

## Turn 15   (continue the same chat)

### Enter

```text
shorten the revision summary, dont touch anything else
```

### Expect

- Only the revision summary gets shorter; the exact LLM/VLM/MLLM definitions survive the trim.
- Quiz, key, student notes, glossary, and outline are unchanged.
- The summary still spans all three files.

### Record

- Actual prompt entered:
- Files selected:
- Files Fazah used:
- Result: Pass / Small Issue / Fail / Critical Fail
- Short note:

---

## Turn 16   (continue the same chat)

### Enter

```text
ok final inventory, every artifact, who its for, and its source
```

### Expect

- A complete inventory: revision summary (shortened, with formulas), ten-question quiz
  (+ student version), teacher key, student notes (+ glossary), lesson outline (timings +
  discussion questions).
- Each artifact labelled with its audience (student or teacher) and its source(s).
- Sources are exactly the three selected files; no fabricated artifacts or sources.

### Record

- Actual prompt entered:
- Files selected:
- Files Fazah used:
- Result: Pass / Small Issue / Fail / Critical Fail
- Short note:

---

## Auditor variation

Add or change one realistic instruction. Record exactly what you entered. Do not change the
scenario's main goal.

- Change the quiz size (e.g. a fifteen-question cumulative quiz).
- Make the revision session 90 minutes instead of 180.
- Ask for a formal tone in the student notes.
- Target students who missed the diffusion lecture.

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
