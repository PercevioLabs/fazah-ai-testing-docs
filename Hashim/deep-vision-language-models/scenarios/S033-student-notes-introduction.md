# S033 — Student notes from the intro deck: audience, length, and exact definitions

## Tests

Sustained multi-turn workflow on ONE set of student notes from the introduction deck: Fazah writes
one-page student-facing notes, preserves the LLM / VLM / MLLM definitions word for word while
simplifying everything else into plain language, adds a "not covered" box and answer-free self-check
questions, produces a separate answer sheet, and holds the one-page limit and student audience
throughout.

## Setup

- Start: New chat
- Select files: `01_dvlm_introduction.pptx`
- Do not select: any other file (especially `AI623_course_outline.pdf` and `13_exam_master_cheatsheet.md`)
- Turns: 8
- Auditor variation: Not allowed

---

## Turn 1

### Enter

```text
make one page of student notes from this intro lecture
```

### Expect

- Student-facing notes are produced, roughly one page.
- Content is grounded in the intro deck (LLM / VLM / MLLM definitions, what the course covers vs
  will NOT cover, grading: 5% attendance / 40% PAs / 35% project / 20% final, open-book open-notes
  assessments), not generic AI material.
- Used source = `01_dvlm_introduction.pptx`; no citation to an unselected file.

### Record

- Actual prompt entered:
- Files selected:
- Files Fazah used:
- Result: Pass / Small Issue / Fail / Critical Fail
- Short note:

---

## Turn 2   (continue the same chat; keep `01_dvlm_introduction.pptx` selected)

### Enter

```text
keep the llm, vlm and mllm definitions exactly how the slides word them, dont paraphrase those
```

### Expect

- The three definitions match the deck: LLM = large model primarily trained on language, able to
  understand text and generate text; VLM = an LLM with a vision encoder, allowing it to understand
  language and images and generate text; MLLM = a more general type of model built to process,
  understand and generate multiple modalities: text, images, video, audio.
- No paraphrasing of these three definitions (e.g. VLM must not become "generates images").
- The rest of the notes are preserved.

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
now simplify everything else into plain language, my students find the slides too dense
```

### Expect

- Everything except the three definitions is rewritten in plain student language.
- The LLM / VLM / MLLM definitions remain exactly as in Turn 2 (not simplified away).
- Facts stay grounded (e.g. course focuses on two modalities, text and images; grading percentages
  unchanged); nothing invented.

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
add a box for what this course will NOT cover
```

### Expect

- A "not covered" box grounded in slide 3: convolutions + attention, CNNs, RNNs, LSTMs,
  transformers, how to train / evaluate / build / deploy AI models.
- Prior notes and exact definitions are preserved.
- The document stays close to one page (or Fazah flags the trade-off).

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
add 3 self check questions at the end, no answers
```

### Expect

- Exactly three self-check questions grounded in the deck (e.g. difference between a VLM and an
  MLLM, what the course will not cover, how the course is graded), with NO answers shown.
- Notes, definitions, and the "not covered" box are preserved.
- Answers appear nowhere in the student notes (answer-leakage check).

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
now a separate answer sheet for me
```

### Expect

- A separate teacher answer sheet answers the three self-check questions, grounded in the deck
  (e.g. VLM understands language + images but generates text; MLLM also handles video and audio).
- The answer sheet matches the questions from Turn 5.
- The student notes remain answer-free (the sheet is a separate document).

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
is the student version still one page? trim it if not, but dont touch the definitions
```

### Expect

- Fazah checks the length and trims to roughly one page if needed.
- The LLM / VLM / MLLM definitions are still word-for-word from the deck after any trimming.
- The self-check questions stay answer-free and the "not covered" box survives (or Fazah says
  explicitly what was cut).

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
confirm which file u used and whats in the final package
```

### Expect

- Fazah names `01_dvlm_introduction.pptx` as the only source and does not claim another file.
- Inventory covers both documents: one-page student notes (student-facing, exact definitions,
  not-covered box, 3 answer-free questions) and the separate teacher answer sheet.
- No fabricated artifacts and no source that was never selected.

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
