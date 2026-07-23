# S002 — No file selected, clear operators topic

## Tests

With no deck selected, the question itself clearly points at PHP operators. Fazah should ground the
answer in the operators deck (`php_operators_presentation (2).pptx`) rather than guessing or
fabricating, then sustain a long, precise workflow — deepening `==` vs `===`, tracing output, building
a comparison table, and turning it all into teacher and student assessment without drifting to other
decks.

## Setup

- Start: New chat
- Select files: none — leave every deck unselected
- Do not select: any deck
- Turns: 12
- Auditor variation: Not allowed

---

## Turn 1

### Enter

```text
explain the arithmetic, comparison and assignment operators
```

### Expect

- Explains arithmetic (`+ - * / %`, `**` power), comparison (`== === != !== < > >= <=`), and
  assignment (`= += -= *= /= %=`) operators, matching the operators deck.
- No deck was selected, so Fazah recognises the topic and grounds in `php_operators_presentation (2).pptx`
  rather than guessing or asking with no basis.
- No fabricated operators and no citation to an unselected or nonexistent deck.

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
go deeper on == vs === , whats the actual difference
```

### Expect

- `==` compares value only; `===` compares value and type — matching the deck.
- Stays grounded in the operators deck; consistent with Turn 1.

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
give me a small code example for each of the 3 categories
```

### Expect

- One short valid PHP example each for arithmetic, comparison, and assignment operators.
- Examples consistent with the deck (e.g. `**` power, `+=`, `===`); no invented functions.

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
trace what this prints: $x = 10; $x %= 3; echo $x;
```

### Expect

- Correctly traces `10 % 3` = 1, so it prints `1`.
- Reasoning consistent with the modulus and assignment operators from prior turns.

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
put == === != !== in a comparison table w what each checks
```

### Expect

- Table of `==` (equal value), `===` (equal value and type), `!=` (not equal value), `!==` (not equal
  value or type) — matching the deck.
- Grounded in the operators deck; nothing invented.

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
which lecture did this come from
```

### Expect

- Names the operators deck (`php_operators_presentation (2).pptx`) as the source used.
- Does not claim a deck that was never provided, and does not hedge that it had no source.

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
ok build 5 short review qs w answers from all this
```

### Expect

- Exactly 5 questions on the operators covered above (arithmetic / comparison / assignment), each with
  a correct answer supported by the operators deck.

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
make 1 of them scenario based
```

### Expect

- Exactly one of the 5 becomes a scenario / applied question; the other four are unchanged.
- Still 5 questions, still grounded in the operators deck.

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
double check each q has exactly 1 correct answer
```

### Expect

- Confirms each of the 5 questions has a single unambiguous correct answer; fixes any that do not.
- Count stays at 5; grounding unchanged.

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
now a student version, no answers
```

### Expect

- The same 5 questions in a student-facing version with NO answers shown
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
and the teacher key w short explanations
```

### Expect

- Teacher key gives the correct answer + a short explanation for each of the 5; the student version
  stays answer-free.

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
just to confirm — all 5 came from the operators slides right, and its still 5
```

### Expect

- Confirms all 5 questions are grounded in the operators deck and the count is still 5.
- Attribution accurate; no drift to other decks.

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
