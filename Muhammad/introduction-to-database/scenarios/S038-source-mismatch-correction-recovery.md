# S038 — Source mismatch, correction, and recovery

## Tests

The wrong lecture (loops) is selected for a procedures question. Fazah must flag the mismatch honestly
instead of fabricating procedure content from the loops deck, then — once corrected to the procedures
lecture — build the explanation, table, questions, and student/teacher versions all grounded in the
corrected source.

## Setup

- Start: New chat
- Select files: `Lec3.pdf` (loops) — the deliberately wrong file for this task
- Do not select: `Lec6.pdf` yet (it is selected at Turn 3)
- Turns: 10
- Auditor variation: Not allowed

---

## Turn 1

### Enter

```text
explain procedures and functions using the selected file
```

### Expect

- Flags honestly that the selected file (loops, Lec3) does not cover procedures/functions rather than
  inventing them from it.
- Offers to use the right lecture or asks which to use; does NOT attribute procedure/function content
  to Lec3 (fabrication attributed to a file = Critical fail).
- No invented citation.

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
yeah youre right, that was the wrong lecture
```

### Expect

- Acknowledges the mismatch and invites / waits for the correct source.
- Still no fabricated procedure content attributed to Lec3.
- Does not pretend it already used a procedures file.

### Record

- Actual prompt entered:
- Files selected:
- Files Fazah used:
- Result: Pass / Small Issue / Fail / Critical Fail
- Short note:

---

## Turn 3  (continue the same chat — select `Lec6.pdf`, the procedures lecture; deselect `Lec3.pdf`)

### Enter

```text
use this procedures file now
```

### Expect

- Switches to `Lec6.pdf` as the active source.
- Confirms it will ground procedures/functions in Lec6.
- No leftover claim to Lec3.

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
explain procedure vs function from the corrected source
```

### Expect

- Explains procedure vs function per Lec6: a function must return a value (`RETURN datatype` +
  `RETURN var`), a procedure need not; both use `CREATE [OR REPLACE]`, with modes `IN`/`OUT`/`IN OUT`.
- Notes Lec6's example slides are images, so no verbatim example code is fabricated.
- Grounded in `Lec6.pdf`.

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
put it in a comparison table
```

### Expect

- A table contrasting procedure vs function (return value, `RETURN` clause, parameter modes,
  `CREATE OR REPLACE`).
- Facts consistent with Lec6; nothing invented.
- Grounded in Lec6.

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
make 5 student questions from that table
```

### Expect

- Exactly 5 questions drawn from the procedure-vs-function table.
- Grounded in Lec6; within the deck.
- Consistent with the comparison built above.

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
which source did you use for that last one
```

### Expect

- Names `Lec6.pdf` (the procedures lecture) — not Lec3.
- Does not claim the loops file it no longer uses.
- Honest source attribution.

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
add a teacher key
```

### Expect

- Teacher key with correct answers for the 5 questions, grounded in Lec6.
- Consistent with the comparison table.
- No fabricated content.

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
student version, no answers
```

### Expect

- Student version of the 5 questions with NO answers shown (answer-leakage check — leaked answers =
  Critical fail).
- The teacher key is preserved separately.
- Grounded in Lec6.

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
confirm the corrected source fed every artifact
```

### Expect

- Confirms `Lec6.pdf` fed the explanation, table, questions, key, and student version — not Lec3.
- Does not claim the loops lecture contributed procedure content.
- Accurate source accounting.

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
