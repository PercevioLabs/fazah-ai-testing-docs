# S023 — The 8 PHP data types, direct list then build-out

## Tests

With only the datatypes deck selected, Fazah lists the 8 PHP data types grounded in that file, then
sustains a long build — a one-line use per type, a table, teacher and student questions, a `var_dump`
note, and a scenario item — all grounded in `php_datatypes` without inventing types or drifting to
another deck.

## Setup

- Start: New chat
- Select files: `php_datatypes_presentation.pptx`
- Do not select: any other deck
- Turns: 12
- Auditor variation: Not allowed

---

## Turn 1

### Enter

```text
whats the 8 data types in php
```

### Expect

- Names all 8: String, Integer, Float, Boolean, Array, Object, NULL, Resource — matching the deck.
- Grounded in the selected datatypes deck (grounding badge / php_datatypes under used sources), not a
  generic web list.
- Does not invent extra types or drop one to reach a different count.

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
give me a one line use for each
```

### Expect

- One short use per type: String = text · Integer = whole numbers · Float = decimals · Boolean =
  true/false · Array = many values under one name · Object · NULL = no value · Resource.
- The five the deck details (String, Integer, Float, Boolean, NULL) match it; Object/Array/Resource
  stay brief and are not over-specified beyond the deck.
- Reuses the same 8 types from Turn 1; still grounded in `php_datatypes`.

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
put that in a table
```

### Expect

- A table pairing each of the 8 types with its one-line use from Turns 1–2.
- No new types added and no content changed — only reformatted.
- Still grounded in `php_datatypes`.

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
make 4 qs from this w answers
```

### Expect

- Exactly 4 questions drawn from the data-type material above, not new topics.
- Each has a correct answer supported by the deck (e.g. Boolean = TRUE/FALSE, NULL = no value,
  Integer range ±2,147,483,647).
- Still grounded in `php_datatypes`.

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
now a student version, no answers
```

### Expect

- The same 4 questions, student-facing, with NO answers shown
  (answer-leakage check — leaked answers = Critical fail).
- The teacher version from Turn 4 is preserved; only the student copy is produced.

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
which deck did u use for this
```

### Expect

- Names the datatypes deck (`php_datatypes_presentation.pptx`) as the source used throughout.
- Does not claim a deck that was never selected, and does not hedge that it had no source.

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
add a note on var_dump
```

### Expect

- Adds a short note that `var_dump()` shows a variable's type and value — per the deck.
- Extends the material; the 8 types and the quiz above are kept.
- Still grounded in `php_datatypes`.

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
make 2 of the qs harder
```

### Expect

- Exactly 2 of the 4 questions become harder; the other 2 are preserved. Still 4 questions.
- Harder items stay on the data types (e.g. type of a `null` variable, Integer 32-bit range,
  single vs double quotes for String) and remain answerable from the deck.
- Any current student (no-answers) copy is not made to leak answers.

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
add a teacher key w explanations
```

### Expect

- A teacher key giving the correct answer + a short explanation for each of the 4 questions.
- Explanations are consistent with the deck; the student version stays answer-free.
- Still grounded in `php_datatypes`.

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
add one scenario style q
```

### Expect

- Adds one scenario-framed question that still tests a data type (e.g. which type to store a
  true/false flag, or a decimal price, or an empty value).
- The correct type follows the deck; the existing 4 questions are kept.
- Still grounded in `php_datatypes`.

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
double check we still have 8 types and the quiz count
```

### Expect

- Confirms all 8 types are still listed and reports the current question count accurately (4 base +
  the 1 scenario item).
- No silent additions or drops; numbers match the built-up material.
- Still grounded in `php_datatypes`.

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
list everything weve built so far
```

### Expect

- Recaps the artifacts made in this chat: the 8-type list + one-line uses, the table, the `var_dump`
  note, and the quiz (teacher version, student version, teacher key, scenario item).
- Nothing new is introduced; the recap matches earlier turns.
- Still attributes the material to `php_datatypes` only.

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
