# S034 — Explicit vs implicit cursor assignment with rubric

## Tests

Across the explicit- and implicit-cursor lectures, Fazah builds a comparison assignment and grows it
demand by demand — instructions, deliverables, criteria, a 4-level rubric, a marks breakdown, a
teacher-only model answer, a submission checklist — while producing a student-facing version that
never exposes the model answer, and finally inventories everything against both sources.

## Setup

- Start: New chat
- Select files: `Lec5.pdf` (explicit cursors), `Lec5_1.pdf` (implicit cursors & SQL cursor
  attributes)
- Do not select: any other lecture
- Turns: 12
- Auditor variation: Not allowed

---

## Turn 1

### Enter

```text
make an assignment comparing explicit and implicit cursors
```

### Expect

- An assignment comparing explicit (Lec5) and implicit (Lec5_1) cursors, drawing on both files.
- Content is accurate: explicit = programmer-declared `DECLARE`/`OPEN`/`FETCH`/`CLOSE` for multi-row;
  implicit = the `SQL` cursor auto-opened for DML / `SELECT INTO` with `SQL%` attributes.
- Grounded in `Lec5.pdf` and `Lec5_1.pdf`; no unselected-file citation.

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
add clear student instructions
```

### Expect

- Clear student instructions are added; the existing comparison content is preserved.
- Instructions stay within the two cursor lectures' scope.

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
add the deliverables - their code + a short write up
```

### Expect

- Deliverables are added: the students' cursor code plus a short write-up; prior content preserved.
- Grounded — asks for explicit/implicit cursor code consistent with the two decks.

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
add grading criteria
```

### Expect

- Grading criteria are added; the rest of the assignment is unchanged.
- Criteria map to the deliverables (code correctness, explicit-vs-implicit understanding).

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
turn the criteria into a 4 level rubric and add a late submission note
```

### Expect

- The criteria are turned into a rubric with exactly 4 levels, and a late-submission note is added.
- The criteria content carries into the rubric; nothing unrelated is changed.

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
produce a student facing final version
```

### Expect

- A student-facing final version (instructions, deliverables, rubric visible) with no teacher-only
  marks scheme or answers.
- Grounded in Lec5/Lec5_1; the teacher content is preserved separately.

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
add a marks breakdown
```

### Expect

- A marks breakdown (points per deliverable/criterion) is added, consistent with the 4-level rubric.
- The rest of the assignment is preserved.

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
add an example of a strong answer, teacher only
```

### Expect

- A strong-answer example is added, clearly marked teacher-only, grounded in Lec5/Lec5_1 (a correct
  explicit + implicit cursor solution).
- No fabricated cursor features; the student-facing version is not yet touched.

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
make sure that example is NOT in the student version
```

### Expect

- Confirms/ensures the strong-answer example is NOT in the student-facing version
  (model answer leaking into the student copy = Critical fail).
- The student version stays free of the model answer.

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
add a submission checklist
```

### Expect

- A submission checklist is added; prior content is preserved.
- The checklist matches the deliverables.

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
shorten the instructions
```

### Expect

- Only the instructions are shortened; deliverables, rubric, marks breakdown, checklist, and the
  teacher-only example are unchanged.
- Still grounded; nothing else altered.

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
give me a final inventory of the assignment, rubric, versions and sources
```

### Expect

- Lists everything produced: the assignment, the 4-level rubric, the marks breakdown, the submission
  checklist, the student-facing version, and the teacher-only example — plus both source files.
- Inventory matches what was actually created; names only `Lec5.pdf` and `Lec5_1.pdf`.

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
