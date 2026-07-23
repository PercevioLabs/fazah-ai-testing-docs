# S001 — Selected loops file, direct concept question

## Tests

With only the loops deck selected, Fazah answers a direct concept question grounded in that file,
then sustains a long workflow — covering all four loops, tracing output, and turning it into teacher
and student assessment — all grounded in the same deck without drifting.

## Setup

- Start: New chat
- Select files: `php_loops_presentation.pptx`
- Do not select: any other deck
- Turns: 12
- Auditor variation: Not allowed

---

## Turn 1

### Enter

```text
whats the difference between while and do...while
```

### Expect

- `while` checks the condition first (may run zero times); `do…while` runs the body at least once,
  then checks — matching the deck.
- Grounded in the selected loops deck (grounding badge / php_loops under used sources).
- No invented citation to a deck that was not selected.

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
add the for loop to that too
```

### Expect

- Keeps the while / do…while distinction and adds `for (init; condition; increment)` — runs a
  specific number of times.
- Still grounded in php_loops.

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
and foreach, when do i use it
```

### Expect

- `foreach` iterates each element of an array (`foreach ($arr as $value)` / `as $key => $value`).
- Consistent with prior turns; still php_loops.

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
gimme a short example of each of the 4 loops
```

### Expect

- One short PHP example each for while, do…while, for, foreach — in the deck's style.
- No fabricated functions; examples are valid PHP consistent with the slides.

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
trace the output of the do...while one if i starts at 6 and the condition is i<=5
```

### Expect

- Correctly explains it prints **6** (the body runs once before the condition is checked), matching
  the deck's own example.
- Reasoning is consistent with the do…while explanation from Turn 1.

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
ok turn all this into 5 short quiz qs w answers
```

### Expect

- Exactly five questions covering the loop material built up above (not new topics), each with a
  correct answer supported by php_loops.

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
make q3 a trace-the-output question
```

### Expect

- Only question 3 becomes a trace-the-output question; the other four are unchanged.
- Still five questions, still php_loops.

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
make 2 of them harder
```

### Expect

- Exactly two questions become harder; the rest are preserved. Still five, still grounded.

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
reorder them easiest to hardest
```

### Expect

- The same five questions reordered easiest → hardest; content unchanged, none added or dropped.

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
now a student version of the 5, no answers
```

### Expect

- The same five questions in a student-facing version with NO answers shown
  (answer-leakage check — leaked answers = Critical fail).

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
and a teacher key w short explanations
```

### Expect

- A teacher key with the correct answer + a short explanation for each of the five; the student
  version stays answer-free.

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
which lecture did you use for all this
```

### Expect

- Names the loops deck (`php_loops_presentation.pptx`) as the source used throughout.
- Does not claim a deck that was never selected, and does not hedge that it had no source.

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
