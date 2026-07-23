# S036 — Loops lesson transformed into teaching assets

## Tests

From the loops lecture, Fazah builds a timed lesson and then spins it into a connected set of teaching
assets — activity, trace scenario, handout, exit tickets, slides, and a revision sheet — keeping every
piece grounded in the same lecture, preserving prior work, and keeping student-facing pieces
answer-free.

## Setup

- Start: New chat
- Select files: `Lec3.pdf` (loops — simple / while / for / nested)
- Do not select: any other lecture
- Turns: 12
- Auditor variation: Not allowed

---

## Turn 1

### Enter

```text
make a 50 min lesson on loops (simple/while/for)
```

### Expect

- Produces a ~50-minute lesson plan on loops covering simple `LOOP` with `EXIT WHEN`, `WHILE`
  (condition-first), and `FOR i IN 1..5` — matching Lec3.
- Time allocation adds toward ~50 min; content stays within the deck.
- Grounded in `Lec3.pdf` (grounding badge / Lec3 under used sources).

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
shorten the teacher explanation to 15 min
```

### Expect

- The teacher-explanation segment is reduced to ~15 min; the other segments are preserved or
  rebalanced.
- Still a loops lesson grounded in Lec3.
- No unrelated sections dropped.

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
add a pair coding activity
```

### Expect

- Adds a pair coding activity (e.g. write a loop / build a nested loop) grounded in Lec3.
- Existing lesson sections preserved.
- No invented constructs beyond the deck.

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
add a real trace-the-output scenario
```

### Expect

- Adds a concrete trace-the-output scenario from the deck (nested loop printing `i||j`, or `mod`
  even/odd), with the correct traced output.
- Prior lesson content preserved.
- Grounded in Lec3.

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
make a one-page student handout
```

### Expect

- A one-page student handout on loops (simple / while / for), student-facing.
- Consistent with the lesson; grounded in Lec3.
- Any embedded practice shows no answers (leakage check).

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
make 5 exit-ticket questions
```

### Expect

- Exactly 5 exit-ticket questions on the loop material.
- Grounded in Lec3; nothing outside loops.
- Consistent with the lesson built so far.

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
make the teacher answers separately
```

### Expect

- Produces the 5 exit-ticket answers as a separate teacher key.
- The student-facing exit tickets and handout stay answer-free (leakage check).
- Grounded in Lec3.

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
add learning objectives
```

### Expect

- Adds learning objectives to the lesson (e.g. distinguish simple/while/for, trace nested loops).
- Existing lesson content preserved.
- Objectives consistent with Lec3.

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
make a 4-slide recap
```

### Expect

- Exactly 4 recap slides on loops.
- Grounded in Lec3; consistent with prior content.
- No content beyond the deck.

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
make a short student revision sheet
```

### Expect

- A short student revision sheet on loops, student-facing with no answers (leakage check).
- Grounded in Lec3.
- Consistent with the lesson.

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
summarize all the assets + confirm same source
```

### Expect

- Lists the assets built (lesson plan, pair activity, trace scenario, handout, 5 exit tickets + key,
  objectives, 4-slide recap, revision sheet).
- Confirms all came from `Lec3.pdf`; no unselected file claimed.
- Accurate inventory.

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
double-check the student handout has no answers
```

### Expect

- Confirms the student handout (and other student-facing pieces) show no answers (answer-leakage
  check — leaked answers = Critical fail).
- Points to the separate teacher key as where the answers live.
- Grounded in Lec3.

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
