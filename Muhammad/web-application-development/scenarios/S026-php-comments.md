# S026 — PHP comment types, distinguish then assess

## Tests

With only the comments deck selected, Fazah distinguishes the three comment forms (`//`, `#`, `/* */`)
and when to use comments, then sustains a build — tiny examples, a table, teacher and student
questions, the "explain WHY not WHAT" best-practice note, and a scenario item — all grounded in
`php_comments` without inventing behaviour.

## Setup

- Start: New chat
- Select files: `php_comments_presentation.pptx`
- Do not select: any other deck
- Turns: 12
- Auditor variation: Not allowed

---

## Turn 1

### Enter

```text
distinguish the comment types // , # and /* */ and when do i use comments
```

### Expect

- `//` and `#` are single-line comments; `/* … */` is multi-line — per the deck.
- A comment is not executed; it is for developers to read. Uses: explain code, disable code,
  documentation blocks.
- Grounded in the selected comments deck (grounding badge / php_comments under used sources).

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
tiny example of each
```

### Expect

- One tiny valid example per form: a `//` line, a `#` line, and a `/* … */` block.
- Examples are valid PHP consistent with the deck.
- Still grounded in `php_comments`.

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
put it in a table
```

### Expect

- A table pairing each comment form with its syntax and whether it is single- or multi-line.
- No new claims added; only reformatted from Turns 1–2.
- Still grounded in `php_comments`.

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
is there a real diff between // and # or same thing
```

### Expect

- States that both `//` and `#` are single-line comment forms in PHP — functionally the same for
  single-line commenting, per the deck; `/* */` remains the multi-line form.
- Does not invent a behavioural difference the deck does not state.
- Still grounded in `php_comments`.

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
make 4 qs, one per idea, w answers
```

### Expect

- Exactly 4 questions, each targeting a distinct idea (single-line `//`, single-line `#`, multi-line
  `/* */`, and why/when to comment — not executed / disable code / document).
- Each has a correct answer supported by the deck.
- Still grounded in `php_comments`.

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
student version no answers
```

### Expect

- The same 4 questions, student-facing, with NO answers shown
  (answer-leakage check — leaked answers = Critical fail).
- The teacher version from Turn 5 is preserved; only the student copy is produced.

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
confirm which deck
```

### Expect

- Names the comments deck (`php_comments_presentation.pptx`) as the source used throughout.
- Does not claim a deck that was never selected, and does not hedge that it had no source.

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
add the best practice note - explain WHY not WHAT
```

### Expect

- Adds the deck's best-practice guidance: comments should explain WHY, not WHAT; keep them concise
  and updated; don't state the obvious or leave sensitive data.
- Extends the material; the comment forms and quiz above are kept.
- Still grounded in `php_comments`.

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
make them harder
```

### Expect

- The 4 questions become harder while staying on the comment material; still exactly 4, still
  answerable from the deck.
- Any current student (no-answers) copy is not made to leak answers.
- Still grounded in `php_comments`.

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
add a teacher key
```

### Expect

- A teacher key with the correct answer + a short explanation for each of the 4 questions.
- Answers follow the deck; the student version stays answer-free.
- Still grounded in `php_comments`.

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
add a scenario q
```

### Expect

- Adds one scenario-framed question (e.g. which comment form to temporarily disable a block of code,
  or to write a documentation block above a function).
- The correct answer follows the deck; the existing 4 questions are kept.
- Still grounded in `php_comments`.

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
verify we still have 3 comment types and the quiz count
```

### Expect

- Confirms the three comment forms (`//`, `#`, `/* */`) are still covered and reports the current
  question count accurately (4 base + the 1 scenario item).
- No silent additions or drops; numbers match the built-up material.
- Still attributes everything to `php_comments` only.

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
