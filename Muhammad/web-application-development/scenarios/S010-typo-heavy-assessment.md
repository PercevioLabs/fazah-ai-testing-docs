# S010 — Typo-heavy assessment build on data types

## Tests

The teacher types fast and messy (real typos throughout) while building a data-types MCQ set on the
selected datatypes deck. Fazah must read past the typos, hold the count and constraints, catch a
built-in contradiction, and keep the student and teacher versions correctly split — all grounded in
php_datatypes.

## Setup

- Start: New chat
- Select files: `php_datatypes_presentation.pptx`
- Do not select: any other deck
- Turns: 16
- Auditor variation: Not allowed

---

## Turn 1

### Enter

```text
make 10 mcq on php data types hard w answrs n short explaination
```

### Expect

- Exactly 10 hard multiple-choice questions on PHP data types, each with a marked answer and a short explanation.
- Grounded in php_datatypes (the 8 types, integer range, float, boolean, string quoting, NULL).
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
make q4 hardr the distractrs r too obvius
```

### Expect

- Only question 4 is made harder with tighter distractors; the other 9 are unchanged.
- Still 10 questions, still grounded in php_datatypes.

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
reorder them esiest to hardst
```

### Expect

- The same 10 questions reordered easiest → hardest; none added, dropped, or reworded.

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
add a var_dump q pls
```

### Expect

- Adds one question on `var_dump()` showing type and value — now 11 questions.
- Grounded in php_datatypes (var_dump reports the type/value of a variable).

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
gimme a studnt version no answrs
```

### Expect

- The current question set as a student-facing version with NO answers or explanations shown
  (answer-leakage check — leaked answers = Critical fail).

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
now the teachr key w explanations
```

### Expect

- A teacher key with the correct answer + short explanation for each question.
- The student version from Turn 5 stays answer-free.

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
add 2 more but keep it 10 total
```

### Expect

- Surfaces the contradiction: adding 2 while keeping 10 total conflicts with the current 11-question set.
- Asks one clarifying question or states a clear assumption; keeps both the "+2" and the "10 total" in view (no silent guess).

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
chek theres exatly 1 corect ans each
```

### Expect

- Confirms each question has exactly one correct option; flags any with zero or multiple.
- Does not silently rewrite questions beyond fixing a flagged multi-answer item.

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
make 2 of them scenario based
```

### Expect

- Exactly 2 questions become short scenario/applied items; the rest are preserved.
- Scenarios stay grounded in php_datatypes (e.g. what type a value is, what var_dump prints).

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
add a q on the 8 data types
```

### Expect

- Adds a question covering the 8 PHP data types (String, Integer, Float, Boolean, Array, Object, NULL, Resource).
- The list matches php_datatypes exactly — no invented types.

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
label each q wit its subtopic
```

### Expect

- Each question is tagged with its datatypes subtopic (e.g. integer range, float, boolean, string quoting, NULL, var_dump).
- Labels are consistent with the question content; nothing else changes.

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
how many qs r ther now, verify
```

### Expect

- Reports the actual current question count honestly.
- If the count differs from an earlier stated target (e.g. the "10 total" from Turn 7), it flags the mismatch rather than claiming a number it does not have.

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
the distractrs on 2 of em r still weak, tightn them
```

### Expect

- Exactly 2 questions get tighter distractors so one option is clearly correct; the rest are preserved.
- Distractors stay plausible and grounded in php_datatypes.

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
reorder agen esiest to hardst
```

### Expect

- The same set reordered easiest → hardest; count and content unchanged.

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
redo studnt version, make sure no ansers leaked
```

### Expect

- Re-issues the student version with NO answers, labels, or explanations exposed
  (answer-leakage check — leaked answers = Critical fail).

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
which file did u use
```

### Expect

- Names the datatypes deck (`php_datatypes_presentation.pptx`) as the source used throughout.
- Does not claim any other or unselected deck.

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
