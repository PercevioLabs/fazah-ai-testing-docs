# S040 — Complete mini course package (long conversation)

## Tests

Across 16 conversational turns Fazah builds a complete mini-unit package over three lectures — plan,
objectives, reading guide, activities, quiz, key, revision sheet, slides, glossary, homework — holding
source grounding, exact counts, audience labels, and no-answer-leakage while producing an accurate
running and final inventory.

## Setup

- Start: New chat
- Select files: `Lec1.pdf` (basics), `Lec3.pdf` (loops), `Lec5.pdf` (explicit cursors)
- Do not select: any other lecture
- Turns: 16
- Auditor variation: Allowed — add or alter exactly one instruction (see Auditor variation below)

## Workflow

```mermaid
flowchart LR
    A[2-week unit plan] --> B[Add objectives and guides]
    B --> C[Cumulative quiz and key]
    C --> D[Slides, glossary, homework]
    D --> E[Student versions, no answers]
    E --> F[Full artifact inventory]
```

---

## Turn 1

### Enter

```text
ok can u make a 2 week mini-unit plan connecting these 3 lectures (basics, loops, cursors)
```

### Expect

- A 2-week mini-unit plan connecting Lec1 (basics: blocks/variables), Lec3 (loops), Lec5 (explicit
  cursors).
- Connections consistent with the decks (blocks underpin loops; cursors fetch multi-row rows in a
  loop).
- Grounded in the three selected files (grounding badge / Lec1, Lec3, Lec5 under used sources).

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
add learning objectives for each week
```

### Expect

- Adds learning objectives for each of the 2 weeks.
- Objectives map to that week's lecture; the existing plan is preserved.
- Grounded in the three files.

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
make a student reading guide
```

### Expect

- A student-facing reading guide across the three lectures.
- Any embedded questions show no answers (leakage check).
- Grounded in the three files.

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
one in-class coding activity per week
```

### Expect

- One coding activity per week (2 total), tied to that week's lecture (e.g. a block/loop, then an
  explicit cursor).
- Activities grounded in Lec1/Lec3/Lec5; existing artifacts preserved.
- No invented constructs.

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
make a 10 question cumulative quiz
```

### Expect

- Exactly 10 questions spanning the three lectures (basics, loops, cursors).
- Grounded in Lec1/Lec3/Lec5; within the decks.
- Consistent with the unit built so far.

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
the teacher answer key
```

### Expect

- Teacher answer key for the 10-question quiz.
- Answers consistent with the three lectures.
- Grounded in the three files.

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
a short student revision sheet
```

### Expect

- A short student revision sheet across the three lectures, student-facing with no answers (leakage
  check).
- Grounded in the three files.
- Consistent with prior content.

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
summarize all the artifacts, who theyre for, and the sources
```

### Expect

- Inventories the artifacts so far (unit plan, objectives, reading guide, 2 activities, 10-q quiz,
  teacher key, revision sheet) with audience (teacher / student) and source lectures.
- Confirms sources are Lec1/Lec3/Lec5 only; no unselected file claimed.
- Accurate audience labels.

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
add a discussion prompt per week
```

### Expect

- Adds one discussion prompt per week (2 total), tied to each week's topic.
- Existing artifacts preserved.
- Grounded in the three files.

### Record

- Actual prompt entered:
- Files selected:
- Files Fazah used:
- Result: Pass / Small Issue / Fail / Critical Fail
- Short note:

---

## Turn 10  (continue the same chat)

### Enter

```text
make a 6-slide overview deck
```

### Expect

- Exactly 6 overview slides across the three lectures.
- Grounded in Lec1/Lec3/Lec5; consistent with prior content.
- Nothing beyond the decks.

### Record

- Actual prompt entered:
- Files selected:
- Files Fazah used:
- Result: Pass / Small Issue / Fail / Critical Fail
- Short note:

---

## Turn 11  (continue the same chat)

### Enter

```text
add a glossary
```

### Expect

- A glossary of key terms from the three lectures (e.g. PL/SQL block, LOOP/WHILE/FOR, explicit cursor,
  `%ROWCOUNT`).
- Definitions consistent with the decks; nothing invented.
- Grounded in the three files.

### Record

- Actual prompt entered:
- Files selected:
- Files Fazah used:
- Result: Pass / Small Issue / Fail / Critical Fail
- Short note:

---

## Turn 12  (continue the same chat)

### Enter

```text
make the quiz student version, no answers
```

### Expect

- Student version of the 10-question quiz with NO answers shown (answer-leakage check — leaked
  answers = Critical fail).
- Questions preserved; the teacher key is not destroyed.
- Grounded in the three files.

### Record

- Actual prompt entered:
- Files selected:
- Files Fazah used:
- Result: Pass / Small Issue / Fail / Critical Fail
- Short note:

---

## Turn 13  (continue the same chat)

### Enter

```text
does the quiz cover all 3 lectures? check it
```

### Expect

- Verifies the 10-question quiz includes items from Lec1 (basics), Lec3 (loops), Lec5 (cursors).
- Reports the per-lecture breakdown; flags any gap honestly.
- Consistent with the quiz.

### Record

- Actual prompt entered:
- Files selected:
- Files Fazah used:
- Result: Pass / Small Issue / Fail / Critical Fail
- Short note:

---

## Turn 14  (continue the same chat)

### Enter

```text
add a homework assignment
```

### Expect

- A homework assignment across the three lectures (e.g. write a block / loop / cursor).
- Grounded in Lec1/Lec3/Lec5; existing artifacts preserved.
- No invented constructs.

### Record

- Actual prompt entered:
- Files selected:
- Files Fazah used:
- Result: Pass / Small Issue / Fail / Critical Fail
- Short note:

---

## Turn 15  (continue the same chat)

### Enter

```text
shorten the reading guide
```

### Expect

- Shortens only the student reading guide; the other artifacts are unchanged.
- Stays student-facing with no answers (leakage check).
- Grounded in the three files.

### Record

- Actual prompt entered:
- Files selected:
- Files Fazah used:
- Result: Pass / Small Issue / Fail / Critical Fail
- Short note:

---

## Turn 16  (continue the same chat)

### Enter

```text
final inventory — every artifact, who its for, and its source
```

### Expect

- A full inventory: each artifact (unit plan, objectives, reading guide, 2 activities, quiz +
  student version + key, revision sheet, discussion prompts, 6-slide deck, glossary, homework), its
  audience, and its source lecture(s).
- Sources limited to Lec1/Lec3/Lec5; no unselected file claimed.
- Consistent with everything built.

### Record

- Actual prompt entered:
- Files selected:
- Files Fazah used:
- Result: Pass / Small Issue / Fail / Critical Fail
- Short note:

---

## Auditor variation

Allowed here: change or add exactly one instruction, then keep the rest of the flow the same and judge
against the adjusted goal. Pick one, for example:

- Make it a 3-week mini-unit instead of 2 weeks (Turn 1) — then weekly objectives, activities, and
  discussion prompts should scale to 3 weeks.
- Change the quiz size (Turn 5), e.g. "make it 8 questions" or "15 questions" — later count and
  coverage checks must match the new number.
- Ask for a formal tone throughout (Turn 1) — wording changes, but sources and answer separation must
  stay correct.
- Target first-year students instead (Turn 1) — reading level adjusts; grounding stays in
  Lec1/Lec3/Lec5.

Whatever you change, the source-grounding, count, and no-answer-leakage checks still apply.

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
