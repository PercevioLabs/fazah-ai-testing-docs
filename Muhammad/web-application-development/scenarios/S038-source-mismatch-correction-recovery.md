# S038 — Source mismatch, correction, and recovery

## Tests

The strings deck is selected but the teacher asks about arrays. Fazah must flag the mismatch honestly
rather than fabricate array content from a strings deck, then recover cleanly once the correct file
(php_arrays) is selected — and, across 20 corrective turns, keep every downstream artifact grounded in
the corrected source, never re-attributing work to the wrong deck, with no answer leakage.

## Setup

- Start: New chat
- Select files: `php_strings_presentation.pptx` (deliberately the wrong deck for the task)
- Do not select: `php_arrays_presentation.pptx` yet (added at Turn 3)
- Turns: 20
- Auditor variation: Not allowed

---

## Turn 1

### Enter

```text
explain arrays using the selected file
```

### Expect

- Flags honestly that the selected deck (php_strings) does not cover arrays; does not fabricate array content and attribute it to the strings deck (fabrication = Critical fail).
- Offers to use the right file or asks which to select; may explain arrays only as clearly-general, un-attributed.

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
yeah youre right, wrong deck
```

### Expect

- Acknowledges the mismatch and waits for / prompts the correct file selection.
- Does not proceed to invent array content in the meantime.

### Record

- Actual prompt entered:
- Files selected:
- Files Fazah used:
- Result: Pass / Small Issue / Fail / Critical Fail
- Short note:

---

## Turn 3  (continue the same chat; deselect php_strings, select php_arrays)

### Enter

```text
use this arrays file now
```

### Expect

- Switches to `php_arrays_presentation.pptx` as the active source.
- Grounds subsequent work in the arrays deck, not the strings deck.

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
explain indexed vs associative from it
```

### Expect

- Explains indexed arrays (numeric index, first = 0) vs associative (named keys `=>`), matching php_arrays.
- Grounded in the corrected arrays deck.

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
make that a comparison table
```

### Expect

- A comparison table contrasting indexed vs associative arrays; facts consistent with the deck.

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
5 student questions from the table
```

### Expect

- Exactly 5 student-facing questions drawn from the table, answerable from php_arrays.
- Student-facing wording; no answers shown here (answer-leakage check — leaked answers = Critical fail).

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
which source did u use for that last one
```

### Expect

- Names `php_arrays_presentation.pptx` (the corrected deck), NOT php_strings.
- Falsely claiming the strings deck (or any unused file) = Critical fail.

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

- A teacher key with the correct answer for each of the 5 questions, grounded in php_arrays.
- The student version stays answer-free.

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

- The 5 questions as a student version with NO answers shown
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
confirm the arrays file fed every artifact so far
```

### Expect

- Confirms the table, questions, teacher key, and student version all came from `php_arrays_presentation.pptx`.
- No artifact attributed to php_strings (false source claim = Critical fail).

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
add a foreach q
```

### Expect

- Adds one `foreach` question (iterating an array), grounded in php_arrays; count now 6.
- Existing questions preserved.

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
verify its there and count is 6
```

### Expect

- Confirms the foreach question exists and the total is 6.

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
make the questions harder
```

### Expect

- The questions are made harder while staying answerable from php_arrays; count unchanged (6).

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
reorder easiest to hardest
```

### Expect

- The same 6 questions reordered easiest → hardest; none added or dropped, content unchanged.

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
add a note on multidimensional arrays
```

### Expect

- A short note on multidimensional arrays (arrays of arrays) added, grounded in php_arrays.

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
add short explanations to the teacher key
```

### Expect

- Each answer in the teacher key gains a short explanation grounded in php_arrays.
- Student version stays answer-free.

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
re-check the student version, no answers
```

### Expect

- Confirms the student version has no answers or key
  (answer-leakage check — any leak = Critical fail).

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
confirm the source again
```

### Expect

- Reconfirms `php_arrays_presentation.pptx` as the source.
- Does not claim php_strings or any other deck (false source claim = Critical fail).

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
final inventory of everything
```

### Expect

- Lists all artifacts (comparison table, 6 questions, teacher key + explanations, student version, multidimensional note).
- Counts match the running set.

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
confirm every artifact used the arrays deck, none from strings
```

### Expect

- Confirms every artifact was built from `php_arrays_presentation.pptx` and none from php_strings.
- Honest about the early mismatch; no false attribution (Critical fail if it claims strings fed any artifact).

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
