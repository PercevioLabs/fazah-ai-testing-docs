# S010 — Typo-heavy assessment request

## Tests

Fazah parses typo-heavy prompts correctly across a full diffusion-quiz workflow — build, add three
targeted questions, convert to MCQ, student/teacher split, and source — without misreading the
misspelled instructions or drifting off the selected diffusion notes.

## Setup

- Start: New chat
- Select files: `06_diffusion_ddpm_ddim_notes.pdf`
- Do not select: any other course file
- Turns: 8
- Auditor variation: Not allowed

---

## Turn 1

### Enter

```text
make a quizz on difussion frm the notes
```

### Expect

- Reads the typos correctly: a quiz on diffusion, grounded in the selected notes.
- Questions come from the diffusion cheat sheet's actual content (schedules α_t = 1−β_t / ᾱ_t,
  forward process, posterior, DDPM vs DDIM sampling) — not generic web material.
- Content is grounded in `06_diffusion_ddpm_ddim_notes.pdf` (grounding badge / used sources).

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
add qustion abt the varaince schedual
```

### Expect

- Reads the intent: add one question about the variance schedule β_t (and its relation
  α_t = 1−β_t, ᾱ_t = ∏α_i) — matching the notes' "variance schedule / noise schedule" section.
- Exactly one question is added; the existing questions are unchanged.
- The new question is answerable from the diffusion notes.

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
n one abt the snr formulla too
```

### Expect

- Adds exactly one question on the signal-to-noise ratio, matching the notes:
  SNR_t = ᾱ_t/(1−ᾱ_t).
- All earlier questions (including the variance-schedule one from turn 2) are preserved.

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
need a q on ddim eta as wel, wat happens at eta 0
```

### Expect

- Adds exactly one question on the DDIM η parameter whose correct answer matches the notes:
  **η = 0 ⇒ σ_t = 0, the noise term disappears, sampling is deterministic**.
- Earlier questions are unchanged; no other content is rewritten.

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
make em all mcq 4 optns 1 corect each
```

### Expect

- Every question in the current quiz becomes multiple-choice with exactly 4 options and exactly
  one correct answer.
- No questions are added or dropped in the conversion; the topics from turns 1–4 (schedule, SNR,
  DDIM η) all survive.
- Distractors are plausible but wrong against the notes (no accidentally-correct second option).

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
studnt copy no ansers pls
```

### Expect

- Produces a student version of the full quiz with NO answers or explanations shown.
- Answer leakage into the student version = Critical fail.
- Same questions and order as turn 5.

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
now techer ky w short explnations
```

### Expect

- Produces a separate teacher key: the same questions with the correct option marked and a short
  explanation each.
- Matches the student version item-for-item (same questions, same order).
- Explanations are consistent with the notes (e.g. SNR_t = ᾱ_t/(1−ᾱ_t); η=0 deterministic).

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
wich file did u use
```

### Expect

- Names the diffusion notes (`06_diffusion_ddpm_ddim_notes.pdf`) as the source.
- Does not claim any other or non-existent file.

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
