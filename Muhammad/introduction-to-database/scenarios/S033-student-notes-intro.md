# S033 — Student notes from the intro lecture

## Tests

From the intro lecture, Fazah produces student-facing notes and refines them iteratively — strip
teacher language, add a glossary within a 2-page limit, add per-section summary boxes, add three
answer-free self-check questions — then makes a separate teacher key while keeping the student
version answer-free, and correctly reports the source and audience.

## Setup

- Start: New chat
- Select files: `Lec1.pdf` (intro: blocks, variables, data types, scope)
- Do not select: any other lecture
- Turns: 8
- Auditor variation: Not allowed

---

## Turn 1

### Enter

```text
make student facing notes from this intro lecture
```

### Expect

- Student-facing notes summarizing Lec1 (what PL/SQL is, the 3-part block, variables, data types,
  scope), grounded in Lec1.
- Reads as notes for students; content matches Lec1 — no loops or cursor material.
- Grounding badge / `Lec1.pdf` under used sources; no invented citation.

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
remove any teacher facing language
```

### Expect

- New version with teacher-facing language removed (no "tell students", "instructor",
  lesson-plan phrasing); the content is otherwise preserved.
- Still grounded in Lec1; same topics, just re-voiced for students.

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
add a glossary and keep it to 2 pages
```

### Expect

- A glossary of Lec1 terms is added (e.g. PL/SQL, block sections, `CONSTANT`, `NOT NULL`,
  `:=` vs `=`) and the notes are limited to ~2 pages.
- Terms are defined per Lec1; earlier content is trimmed to fit, not swapped for new topics.

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
add a summary box per section
```

### Expect

- A summary box is added to each section; section content is preserved.
- Boxes accurately summarize Lec1 material; still within the ~2-page limit.

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
add 3 self check questions, no answers
```

### Expect

- Exactly 3 self-check questions are added with NO answers shown
  (answer-leakage check — leaked answers = Critical fail).
- Questions are grounded in Lec1; the rest of the notes is preserved.

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
now make a teacher key for those
```

### Expect

- A separate teacher key with correct answers/explanations for the 3 self-check questions, grounded
  in Lec1.
- The student notes remain answer-free.

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
double check the student version still has no answers
```

### Expect

- Confirms the student version still shows no answers for the 3 self-check questions
  (any leak = Critical fail).
- Reports honestly; does not quietly alter content just to pass the check.

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
confirm which file this is from + who the notes are for
```

### Expect

- Names `Lec1.pdf` as the source and states the notes are student-facing (for students).
- Does not claim an unselected lecture or hedge that it had no source.

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

For the complete workflow, see [Context Diagram](../misc/CONTEXT-DIAGRAM.md).
