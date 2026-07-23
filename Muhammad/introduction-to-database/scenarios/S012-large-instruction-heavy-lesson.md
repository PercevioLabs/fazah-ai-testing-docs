# S012 — Large instruction-heavy lesson plan, procedures lecture

## Tests

From one big, demanding, heavily-constrained prompt, Fazah builds a timed 45-minute procedures &
functions lesson, then adjusts timings, adds a task, expands prep notes, swaps the exit ticket, and
splits student handout from answer key — all grounded only in Lec6.

## Setup

- Start: New chat
- Select files: `Lec6.pdf` (procedures & functions)
- Do not select: any other lecture
- Turns: 8
- Auditor variation: Not allowed

---

## Turn 1

### Enter

```text
need a 45 min lesson on procedures & functions for undergrads. must have 3 measurable objectives, a 5 min opening, 15 min explanation, 10 min coding task, 5 min debrief, and a 5 min exit ticket. use the procedures lecture only. include teacher prep notes.
```

### Expect

- A 45-minute lesson plan with 3 measurable objectives and timed sections: 5-min opening, 15-min
  explanation, 10-min coding task, 5-min debrief, 5-min exit ticket, plus teacher prep notes.
- Content grounded in Lec6: procedures & functions, `IN` / `OUT` / `IN OUT`, `CREATE OR REPLACE`,
  a function's `RETURN`.
- Grounded in `Lec6.pdf`, procedures/functions only; no fabricated verbatim deck example code
  (Lec6 example slides are images).

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
shorten the explanation to 10 min
```

### Expect

- The explanation section is changed to 10 minutes; the rest of the plan is preserved.
- Timings updated coherently; still a procedures & functions lesson from Lec6.

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
add a 2nd coding task
```

### Expect

- A second coding task added, grounded in Lec6 (write a procedure/function using `IN`/`OUT`/`IN OUT`,
  `CREATE OR REPLACE`, or a function `RETURN`).
- The prior structure and first coding task are preserved.

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
give me more detailed teacher prep notes
```

### Expect

- Teacher prep notes expanded, still accurate to Lec6 (procedure has no `DECLARE` keyword; no data size
  in a procedure's declaration; function must return a value).
- No fabricated verbatim example code; rest of the plan preserved.

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
swap the exit ticket for 3 short qs
```

### Expect

- The exit ticket is replaced by 3 short questions on procedures / functions.
- Grounded in Lec6; the rest of the plan preserved.

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
make a student handout for this
```

### Expect

- A student-facing handout for the lesson.
- If the 3 questions appear, no answers are leaked into the student handout (answer-leakage check).
- Content grounded in Lec6.

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
now give me an answer key for those 3 qs separately
```

### Expect

- A separate answer key for the 3 questions, answers grounded in Lec6.
- Kept separate from the student handout (which stays answer-free).

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
confirm this only used the procedures lecture
```

### Expect

- Confirms `Lec6.pdf` (procedures & functions) was the only source used.
- Does not claim any other lecture.

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
