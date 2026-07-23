# S016 — Informal refinement language (type casting)

## Tests

A teacher iterates in short, informal nudges ("way simpler", "keep the def") on type casting with
nothing selected. Fazah must recognise the casting material, ground everything in the casting deck
without being told, hold the definition steady while the framing changes, and keep the student and
teacher versions split.

## Setup

- Start: New chat
- Select files: none (start with nothing selected)
- Do not select: leave everything unselected — Fazah must find the right deck itself
- Turns: 14
- Auditor variation: Allowed (see the Auditor variation section below)

---

## Turn 1

### Enter

```text
explain type casting
```

### Expect

- Explains type casting as converting a value's type, e.g. `(int) (string) (bool) (float) (array)`,
  verifiable with `var_dump()` — matching php_casting.
- With no file selected, grounds the answer in the casting deck (php_casting) rather than guessing.
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
no make it way simpler
```

### Expect

- Simplifies the wording while keeping the casting facts correct.
- Still grounded in php_casting; nothing made incorrect in the process.

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
give a real analogy but dont change the definition
```

### Expect

- Adds a plain-language analogy for casting while leaving the definition intact.
- The analogy is a teaching device, not attributed as a verbatim quote from the deck.

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
ok now a 4 line summary
```

### Expect

- A 4-line summary of type casting grounded in php_casting.
- Keeps the definition consistent with the earlier turns.

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
3 quick qs
```

### Expect

- Exactly 3 short questions on type casting, each with a correct answer supported by php_casting.
- Grounded (e.g. `(int) 5.34` → 5, `(int) "25 km"` → 25, falsy values).

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
keep the def but gimme a student version, no answers
```

### Expect

- The 3 questions as a student-facing version with NO answers shown; the definition is preserved
  (answer-leakage check — leaked answers = Critical fail).

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
what lecture is this
```

### Expect

- Names the casting deck (`php_casting_presentation.pptx`) as the source, even though it was never manually selected.
- Does not claim a different or unselected deck, and does not say it had no source.

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
add an (int) truncation example, like 5.34
```

### Expect

- Adds a valid example: `(int) 5.34` truncates to `5` — matching php_casting.
- Does not overwrite the summary or questions already built.

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
make the qs harder
```

### Expect

- The 3 questions become harder (e.g. truthy/falsy edge cases, string-to-int extraction); still 3.
- Still grounded in php_casting.

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
teacher key
```

### Expect

- A teacher key with the correct answer + short explanation for each of the 3 questions.
- The student version from Turn 6 stays answer-free.

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
add the truthy falsy example too, the ones that come out false
```

### Expect

- Adds an example of falsy values that cast to `false`: `0`, `0.0`, `""`, `"0"`, `NULL`, `false`, `[]`
  — matching php_casting.
- Does not misstate any of these (e.g. `"0"` is falsy, but `"0.0"` as a string is truthy).

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
change the analogy to something else
```

### Expect

- Swaps in a different analogy while keeping the definition unchanged.
- Still a teaching device, not attributed as a deck quote.

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
make the summary one paragraph
```

### Expect

- Condenses the summary to a single paragraph while keeping the casting facts and definition intact.
- Still grounded in php_casting.

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
redo the student version, make sure no answers show
```

### Expect

- Re-issues the 3 questions as a student version with NO answers or explanations exposed
  (answer-leakage check — leaked answers = Critical fail).

### Record

- Actual prompt entered:
- Files selected:
- Files Fazah used:
- Result: Pass / Small Issue / Fail / Critical Fail
- Short note:

---

## Auditor variation

Add or change one realistic instruction. Record exactly what you entered. Do not change the scenario's
main goal.

Examples:

- Make it shorter.
- Change the analogy.
- Add one more example.
- Condense it to one paragraph.

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
