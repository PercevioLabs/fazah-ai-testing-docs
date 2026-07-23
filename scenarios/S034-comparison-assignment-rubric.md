# S034 — Plan-driven vs. agile assignment with rubric, built over many turns

## Tests

Sustained multi-turn workflow on ONE comparison assignment across two decks: Fazah adds instructions,
deliverables, and grading criteria, converts them into a four-level rubric with a late note and a marks
breakdown, keeps a teacher-only strong-answer example out of the student version, adds a checklist and
trims the instructions, then closes with an honest inventory — preserving prior work at every step.

## Setup

- Start: New chat
- Select files: `Ch2 SW Processes.pptx`, `Ch5 Agile SW Dev.pptx`
- Do not select: `Ch1 Introduction.pptx`, `Ch3 Req Eng.pptx`, `Ch4 Testing.pptx`
- Turns: 12
- Auditor variation: Not allowed

---

## Turn 1

### Enter

```text
Create an assignment comparing plan-driven and agile development.
```

### Expect

- An assignment is produced with a plan-driven vs. agile comparison focus.
- Content is grounded in the Processes and Agile decks (e.g. plan-driven vs. agile, waterfall vs.
  incremental, Agile Manifesto/XP/Scrum), not generic material.
- The task is a coherent starting point for later additions.

### Record

- Actual prompt entered:
- Files selected:
- Files Fazah used:
- Result: Pass / Small Issue / Fail / Critical Fail
- Short note:

---

## Turn 2   (continue the same chat; keep both files selected)

### Enter

```text
Add clear student instructions.
```

### Expect

- Clear student instructions are added.
- The Turn 1 assignment content is preserved.
- The change is a new version of the same assignment.

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
Add the deliverables.
```

### Expect

- A deliverables section is added.
- The instructions and assignment from earlier turns are preserved.
- No unrelated content is changed.

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
Add grading criteria.
```

### Expect

- Grading criteria are added.
- The deliverables, instructions, and assignment are all preserved.
- No unrelated content is changed.

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
Turn the grading criteria into a four-level rubric and add a late-submission note.
```

### Expect

- The grading criteria become a four-level rubric derived from those criteria.
- A late-submission note is added.
- All prior content (assignment, instructions, deliverables) is preserved.

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
Produce a student-facing final version.
```

### Expect

- A student-facing final version is produced, consistent with all earlier edits.
- No teacher-only notes leak into the student version (audience-leakage check).
- The rubric and instructions remain usable for students.

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
Add a marks breakdown.
```

### Expect

- A marks breakdown is added, consistent with the four-level rubric weighting.
- The breakdown totals coherently and maps to the deliverables/criteria.
- Prior sections are preserved; only the breakdown is added.

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
Add an example of a strong answer, for teachers only.
```

### Expect

- A strong-answer example is added, marked teacher-only, grounded in the two decks.
- The example is placed in the teacher-facing material, not the student version.
- Assignment, rubric, and marks breakdown are preserved.

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
Make sure that example is not in the student version.
```

### Expect

- Fazah confirms the strong-answer example is absent from the student-facing version.
- The student version still has the assignment, instructions, deliverables, and rubric.
- Any leak of the example into the student version is removed (answer-leakage check).

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
Add a submission checklist.
```

### Expect

- A submission checklist is added, matching the deliverables.
- The checklist appears in the student-facing version (it is student guidance).
- The teacher-only example stays out of the student version.

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
Shorten the instructions.
```

### Expect

- Only the instructions are made shorter.
- The deliverables, rubric, marks breakdown, and checklist are unchanged.
- The teacher-only example is still separate from the student version.

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
Give me a final inventory of the assignment, rubric, versions, and the sources you used.
```

### Expect

- Fazah lists the assignment, four-level rubric, student version, teacher version, and checklist.
- It names `Ch2 SW Processes.pptx` and `Ch5 Agile SW Dev.pptx` and no other deck.
- The inventory matches what was actually produced; nothing is invented.

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

For the complete workflow, see [Context Diagram](../CONTEXT-DIAGRAM.md).
