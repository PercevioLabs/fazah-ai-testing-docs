# S019 — "Use these slides" with nothing selected

## Tests

A deictic "use these slides" with no file selected has no referent; Fazah should ask which source
rather than invent one, then — once Lec4 is selected — build SELECT INTO / %TYPE / %ROWTYPE
questions grounded in Lec4 and sustain answers, an item edit, a reorder, a student version, and a
source confirmation.

## Setup

- Start: New chat
- Select files: none at first; select `Lec4.pdf` (SELECT INTO, %TYPE, %ROWTYPE) at Turn 2
- Do not select: any file at Turn 1 — the missing referent for "these slides" is the point
- Turns: 7
- Auditor variation: Not allowed

---

## Turn 1

### Enter

```text
use these slides and make 5 questions
```

### Expect

- Notes that nothing is selected / "these slides" has no referent, and asks which file (or slides) to
  use.
- Does not invent a source or fabricate 5 questions from an unnamed deck.
- No questions generated yet — with nothing selected, making up content is not acceptable here.

### Record

- Actual prompt entered:
- Files selected:
- Files Fazah used:
- Result: Pass / Small Issue / Fail / Critical Fail
- Short note:

---

## Turn 2  (continue the same chat — select `Lec4.pdf`)

### Enter

```text
these ones
```

### Expect

- Recognizes `Lec4.pdf` (SELECT INTO, %TYPE, %ROWTYPE, aggregates) as the now-selected source.
- Produces exactly 5 questions grounded in Lec4 — `SELECT ... INTO`, `%TYPE`, `%ROWTYPE`,
  `MAX/MIN` aggregates, HR `employees`/`jobs`.
- No fabricated columns/tables beyond the deck; grounded in `Lec4.pdf`.

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
add answers to each
```

### Expect

- The same 5 questions are kept; each gets a correct answer supported by Lec4.
- Answers stay within Lec4 content (single-row read, %TYPE vs %ROWTYPE, aggregates).
- Still grounded in `Lec4.pdf`.

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
turn question 2 into a trace-the-output question
```

### Expect

- Only question 2 changes — into a trace-the-output exercise (e.g. trace a `SELECT INTO` /
  aggregate result), grounded in Lec4.
- The other 4 questions are unchanged; still 5 total.
- Its answer is updated to match; still grounded in `Lec4.pdf`.

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
reorder foundational to advanced
```

### Expect

- The same 5 questions are reordered easy→hard (e.g. `SELECT INTO`/`%TYPE` first, `%ROWTYPE`/
  aggregate/trace later); content unchanged, only order.
- Nothing dropped or added; still 5 with their answers intact.

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
student version, no answers
```

### Expect

- The same 5 questions in a student-facing version with NO answers shown
  (answer-leakage check — leaked answers = Critical fail).
- The teacher version with answers is preserved; only the student copy is produced.

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
confirm which source these came from
```

### Expect

- Names `Lec4.pdf` as the source used.
- Does not claim a file that was never selected — in particular not the "these slides" phantom from
  Turn 1 — and does not say it had no source.

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
