# S034 — Forms + arrays assignment with rubric, demanding build

## Tests

With forms and arrays selected, Fazah builds an assignment (an HTML form that stores submissions in an
array) and then survives a demanding 24-turn build — instructions, deliverables, a 4-level rubric with
weightings, a teacher-only strong-answer example, security/`$_POST`/`foreach` requirements, an
extension task, and a submission checklist — always grounding in the two selected decks and keeping
the teacher-only model answer out of the student-facing version.

## Setup

- Start: New chat
- Select files: `php_forms_presentation.pptx`, `php_arrays_presentation.pptx`
- Do not select: any other deck
- Turns: 24
- Auditor variation: Not allowed

---

## Turn 1

### Enter

```text
need an assignment: build an HTML form that stores submissions in an array
```

### Expect

- Produces an assignment brief: build an HTML form (`<form action method>`, inputs) that stores submissions in an array.
- Grounded in php_forms + php_arrays; no other deck.

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

- Adds clear, step-by-step student instructions for building the form and storing submissions in an array.
- Grounded; unambiguous.

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
add deliverables — their php code + a short write up
```

### Expect

- Adds a deliverables list: the student's PHP code and a short write-up.
- Consistent with the task.

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

- Adds grading criteria tied to the deliverables (form correctness, array usage, write-up, etc.).
- Grounded.

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

- Converts the criteria into a 4-level rubric (e.g. excellent → poor) and adds a late-submission policy note.
- The criteria are preserved as rubric rows.

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
gimme a student facing final version
```

### Expect

- Produces the student-facing assignment (instructions, deliverables, rubric, late note) with no
  teacher-only material (answer-leakage check — leaked model answers = Critical fail).
- Grounded.

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

- Adds a marks/points breakdown across the rubric criteria (summing to the assignment total).
- Consistent with the 4-level rubric.

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
add a teacher only strong answer example
```

### Expect

- Adds a model/strong-answer example marked teacher-only (valid PHP form + array storage, e.g. with `foreach`).
- Grounded; clearly flagged teacher-only.

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

- Confirms the strong-answer example is excluded from the student-facing version
  (answer-leakage check — leaked model answers = Critical fail).
- The example is kept in the teacher-only doc.

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

- Adds a student submission checklist (form works, stores in array, code + write-up attached).
- Consistent with the deliverables.

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
the instructions are too long, shorten them
```

### Expect

- Shortens the instructions while keeping them clear and complete.
- Other sections are unchanged.

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
list everything we have so far
```

### Expect

- Inventory: brief, instructions, deliverables, 4-level rubric + marks breakdown + late note, teacher-only
  example, submission checklist, student-facing version.
- Matches produced content; no invented items.

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
add a security requirement, they must validate and sanitize input
```

### Expect

- Adds a requirement to validate and sanitize form input (never trust user input), grounded in php_forms.
- Reflected in the instructions/deliverables and the rubric where relevant.

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
require them to use $_POST
```

### Expect

- Adds a requirement to use `$_POST` for the form (POST recommended for forms; not in URL), grounded in php_forms.
- Consistent with the form task.

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
confirm the rubric still has 4 levels
```

### Expect

- Confirms the rubric has exactly 4 levels after the edits.
- The criteria remain intact.

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
redo the student version, no teacher stuff in it
```

### Expect

- Updated student-facing version including the new requirements, with no teacher-only example/answers
  (answer-leakage check — leaked model answers = Critical fail).

### Record

- Actual prompt entered:
- Files selected:
- Files Fazah used:
- Result: Pass / Small Issue / Fail / Critical Fail
- Short note:

---

## Turn 17  (continue the same chat)

### Enter

```text
add an extension task for strong students
```

### Expect

- Adds an extension task (e.g. a multidimensional array, or displaying submissions with `foreach`), grounded.
- Clearly marked as an extension.

### Record

- Actual prompt entered:
- Files selected:
- Files Fazah used:
- Result: Pass / Small Issue / Fail / Critical Fail
- Short note:

---

## Turn 18  (continue the same chat)

### Enter

```text
require a foreach to display the stored submissions
```

### Expect

- Adds a requirement to display the stored submissions using `foreach` (iterate the array), grounded in php_arrays.
- Consistent with the array-storage task.

### Record

- Actual prompt entered:
- Files selected:
- Files Fazah used:
- Result: Pass / Small Issue / Fail / Critical Fail
- Short note:

---

## Turn 19  (continue the same chat)

### Enter

```text
check the deliverables list is still complete
```

### Expect

- Confirms the deliverables (PHP code + write-up, now including security/`$_POST`/`foreach`) are complete and consistent.
- Nothing dropped.

### Record

- Actual prompt entered:
- Files selected:
- Files Fazah used:
- Result: Pass / Small Issue / Fail / Critical Fail
- Short note:

---

## Turn 20  (continue the same chat)

### Enter

```text
which files did u use
```

### Expect

- Names `php_forms_presentation.pptx` and `php_arrays_presentation.pptx` as the sources.
- No unselected deck claimed.

### Record

- Actual prompt entered:
- Files selected:
- Files Fazah used:
- Result: Pass / Small Issue / Fail / Critical Fail
- Short note:

---

## Turn 21  (continue the same chat)

### Enter

```text
add points/weighting to each rubric level
```

### Expect

- Adds point weightings to the rubric criteria/levels; totals consistent with the marks breakdown.
- The 4 levels are preserved.

### Record

- Actual prompt entered:
- Files selected:
- Files Fazah used:
- Result: Pass / Small Issue / Fail / Critical Fail
- Short note:

---

## Turn 22  (continue the same chat)

### Enter

```text
make the extension task optional bonus marks
```

### Expect

- Marks the extension task as optional/bonus, separate from the core total.
- The core marks breakdown is unchanged.

### Record

- Actual prompt entered:
- Files selected:
- Files Fazah used:
- Result: Pass / Small Issue / Fail / Critical Fail
- Short note:

---

## Turn 23  (continue the same chat)

### Enter

```text
final student version, triple check no strong-answer example in it
```

### Expect

- Final student-facing version confirmed free of the teacher-only strong-answer example and any solutions
  (answer-leakage check — leaked model answers = Critical fail).

### Record

- Actual prompt entered:
- Files selected:
- Files Fazah used:
- Result: Pass / Small Issue / Fail / Critical Fail
- Short note:

---

## Turn 24  (continue the same chat)

### Enter

```text
final inventory — confirm 4 level rubric, deliverables, sources, nothing leaked
```

### Expect

- Final inventory of all assets; confirms the 4-level rubric (with weightings), the full deliverables,
  the sources (forms + arrays), and the teacher-only example kept separate.
- Confirms no leakage into the student version (answer-leakage check — leaked model answers = Critical fail).

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
