# S004 — Two files selected, structured comparison

## Tests

With the if/else and switch decks both selected, Fazah builds a structured comparison strictly from
those two files — table, syntax row, the fall-through note, code and a trace — then turns it into a
4-question assessment with student and teacher versions, never pulling from any other deck.

## Setup

- Start: New chat
- Select files: `php_if_else_presentation.pptx` and `php_switch_presentation.pptx`
- Do not select: any other deck
- Turns: 14
- Auditor variation: Not allowed

---

## Turn 1

### Enter

```text
compare if/elseif and switch in a table — when to use each, plus one example each. use only the selected slides
```

### Expect

- Table contrasting `if / elseif / else` (multiple conditions / ranges) vs `switch` (one expression
  compared to many cases), with a when-to-use note and one example each.
- Grounded only in the two selected decks (`php_if_else`, `php_switch`); nothing pulled from other files.

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
add a syntax row to the table
```

### Expect

- Adds a syntax row: `if (cond) { } elseif (cond) { } else { }` vs
  `switch (expr) { case label: … break; default: … }` — matching the decks.
- Rest of the table preserved.

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
add a note about fall-through — switch w/o break
```

### Expect

- Notes that omitting `break` causes fall-through (subsequent cases run) — matching the switch deck.
- Grounded; no fabrication.

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
give a full code example for each
```

### Expect

- One valid `if / elseif / else` example (e.g. the hour-based greeting) and one `switch` example with
  `case` / `break` / `default`, consistent with the decks.
- No invented syntax.

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
trace the switch example if i drop the break on the first case
```

### Expect

- Correctly shows fall-through: the matched case plus the following case(s) run until a `break` or the
  end — consistent with Turn 3.
- Grounded in the switch deck.

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
make 4 quiz qs from this
```

### Expect

- Exactly 4 questions on if/elseif vs switch (including fall-through), each with a correct answer
  supported by the two decks.

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
make one of them scenario based
```

### Expect

- Exactly one of the 4 becomes a scenario question; the others unchanged.
- Still 4, still grounded in the two decks.

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

- Exactly two of the 4 become harder; the rest preserved.
- Still 4, still grounded.

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
reorder easiest to hardest
```

### Expect

- The same 4 questions reordered easiest → hardest; none added or dropped.

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
check each has exactly 1 right answer
```

### Expect

- Confirms each of the 4 has a single correct answer; fixes any ambiguity.
- Count stays at 4; grounding unchanged.

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
student version now, no answers
```

### Expect

- The same 4 questions, student-facing, with NO answers shown
  (answer-leakage check — leaked answers = Critical fail).

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
teacher key w explanations
```

### Expect

- Teacher key: correct answer + short explanation for each of the 4; the student version stays
  answer-free.

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
confirm you only used the 2 selected decks, nothing else
```

### Expect

- Confirms only `php_if_else` and `php_switch` were used; no other deck contributed.
- Attribution accurate.

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
which 2 files exactly
```

### Expect

- Names both decks: `php_if_else_presentation.pptx` and `php_switch_presentation.pptx`.
- No extra or invented files.

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
