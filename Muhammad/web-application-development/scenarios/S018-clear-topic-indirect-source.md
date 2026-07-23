# S018 — Clear topic named indirectly ("the lecture about numbers")

## Tests

A teacher names a topic indirectly ("the lecture about numbers") without selecting a file. Fazah must
map that to the correct deck (`php_numbers`) and stay grounded there through a long explanation → quiz
workflow, correctly stating which file it mapped to when asked and never leaking answers in the
student version.

## Setup

- Start: New chat
- Select files: none (Fazah must map "the lecture about numbers" to `php_numbers_presentation.pptx`)
- Do not select: any deck (do not pre-select the mapping)
- Turns: 12
- Auditor variation: Not allowed

---

## Turn 1

### Enter

```text
use the lecture about numbers and explain integers vs floats vs numeric strings
```

### Expect

- Maps "the lecture about numbers" to `php_numbers` and grounds there (does not invent a source).
- Explains integer (whole numbers, 32-bit range, decimal/hex/octal/binary), float (decimal or
  exponential like `7.64E+5`), and numeric strings — matching the deck.

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
give a short example of each
```

### Expect

- One short PHP example each for an integer, a float, and a numeric string.
- Valid PHP consistent with the deck; no fabricated functions.

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
add a note on is_numeric
```

### Expect

- Notes that `is_numeric()` checks whether a value is a number or a numeric string — from the deck.
- Stays grounded in php_numbers (may mention related `is_infinite`/`is_finite`/`is_nan` only as in the slides).

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
ok make 3 questions on this
```

### Expect

- Exactly three questions grounded in php_numbers (integers / floats / numeric strings / is_numeric).
- No answers shown yet; no new topics introduced.

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
add the answers
```

### Expect

- One correct answer per question, each supported by php_numbers.
- Still exactly three questions.

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
which file did you map that to
```

### Expect

- Names `php_numbers_presentation.pptx` as the file it mapped "the lecture about numbers" to.
- Does not claim any other deck and does not hedge that it had no source.

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
add a note about hex and octal too
```

### Expect

- Adds that integers can be written in hex (`0xFF`) and octal (`0377`) — and binary (`0b…`) — per the deck.
- Consistent with the earlier integer explanation; still php_numbers.

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
make the 3 questions harder
```

### Expect

- All three become harder while still covering the same number material; still exactly three.
- Answers remain correct and grounded in php_numbers.

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
now a student version, no answers
```

### Expect

- The same three questions in a student-facing version with NO answers shown
  (answer-leakage check — leaked answers = Critical fail).

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
and a teacher key with short explanations
```

### Expect

- A teacher key with the correct answer + a short explanation for each of the three, grounded in php_numbers.
- The student version stays answer-free.

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
check each question has exactly one correct answer
```

### Expect

- Confirms each of the three has a single correct answer; flags any that don't.
- No new fabricated content introduced during the check.

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
quick inventory of what we built and which deck
```

### Expect

- Lists what was made: a 3-question number quiz, a student version (no answers), and a teacher key.
- Names the single source: `php_numbers_presentation.pptx`.

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
