# S009 — Extremely short prompts, no file selected

## Tests

A teacher fires terse one- or two-word fragments with nothing selected. Fazah must infer that the
target is the loops material, ground every answer in the loops deck without being told, and sustain a
full explain → example → quiz → student/teacher split arc — then correctly name the source at the end.

## Setup

- Start: New chat
- Select files: none (start with nothing selected)
- Do not select: leave everything unselected — Fazah must find the right deck itself
- Turns: 10
- Auditor variation: Not allowed

---

## Turn 1

### Enter

```text
explain for loop
```

### Expect

- Explains `for (init; condition; increment)` runs a set number of times — matching php_loops.
- With no file selected, grounds the answer in the loops deck (php_loops) rather than guessing.
- No invented citation to a deck that was never selected.

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
syntax?
```

### Expect

- Shows the `for (init; cond; increment) { }` structure with a minimal valid PHP example.
- Consistent with Turn 1; still loops material.

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
count down example
```

### Expect

- Gives a counting-down `for` loop, e.g. `for ($i = 5; $i >= 1; $i--)` — valid PHP.
- Matches the deck's "count up / down" use of `for`.

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
skip by 2
```

### Expect

- Adjusts the loop to step by 2, e.g. `for ($i = 0; $i <= 10; $i += 2)`.
- The deck notes `for` can skip by 2; the example is valid and consistent with prior turns.

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
hows foreach diff
```

### Expect

- Explains `foreach ($arr as $value)` / `as $key => $value` iterates array elements without a manual counter.
- Contrasts with `for`; still grounded in php_loops.

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
make 3 quick qs
```

### Expect

- Exactly 3 short questions on the for / foreach material built up above, not new topics.
- Each has a correct answer supported by php_loops.

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
make em harder
```

### Expect

- All 3 questions become harder (e.g. trace-the-output / step-by-2 edge cases); still 3 questions.
- Still grounded in the loops material.

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
student version no answers
```

### Expect

- The same 3 questions in a student-facing version with NO answers shown
  (answer-leakage check — leaked answers = Critical fail).

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
teacher key
```

### Expect

- A teacher key with the correct answer + a short explanation for each of the 3.
- The student version from Turn 8 stays answer-free.

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
which lecture?
```

### Expect

- Names the loops deck (`php_loops_presentation.pptx`) as the source used throughout.
- Does not claim a different or unselected deck, and does not say it had no source.

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
