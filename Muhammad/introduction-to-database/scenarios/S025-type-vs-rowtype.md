# S025 — %TYPE vs %ROWTYPE, iterative self-check build

## Tests

With only the `SELECT INTO` / attribute lecture selected, Fazah explains `%TYPE` vs `%ROWTYPE`, grounds
an HR example in the deck's employees/jobs schema, and iterates a self-check into a teacher key and a
clean student version — plus a rationale note and one extra question — all grounded in Lec4.

## Setup

- Start: New chat
- Select files: `Lec4.pdf` (`SELECT ... INTO`, `%TYPE`, `%ROWTYPE`, aggregates)
- Do not select: any other lecture
- Turns: 8
- Auditor variation: Not allowed

---

## Turn 1

### Enter

```text
whats the difference between %type and %rowtype
```

### Expect

- `%TYPE` = a variable with the same type as a single column; `%ROWTYPE` = a record shaped like a
  whole row — per Lec4.
- Grounded in the selected lecture (grounding badge / Lec4 under used sources), not a generic answer.
- No fabricated syntax beyond the deck.

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
give an hr example of each - employees / jobs
```

### Expect

- `%TYPE` example like `i employees.employee_id%TYPE;`; `%ROWTYPE` example like `job_rec jobs%ROWTYPE;`
  read via `job_rec.min_salary` / `job_rec.max_salary` — matching Lec4's HR schema.
- Uses only deck columns (employee_id, min_salary, max_salary); no invented columns/tables.
- Still grounded in `Lec4.pdf`.

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
turn this into a short student self-check
```

### Expect

- A short self-check (a handful of items) on `%TYPE` / `%ROWTYPE` built from the material above, not
  new topics.
- Items are answerable from Lec4; no content invented beyond the deck.
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
now make a teacher key for the self-check
```

### Expect

- An answer key for the same self-check items from Turn 3 (keeps the set, adds correct answers).
- Each answer is supported by Lec4 (`%TYPE` = column type, `%ROWTYPE` = row record).
- Still grounded in `Lec4.pdf`.

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

- The same self-check items, student-facing, with NO answers shown
  (answer-leakage check — leaked answers = Critical fail).
- The teacher key from Turn 4 is preserved; only the student copy is produced.

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
add a note on why we use %type instead of hardcoding the type
```

### Expect

- A short note: `%TYPE` avoids hard-coding a column's data type, so the variable tracks the column
  definition — per Lec4.
- Extends the material; the earlier items and key are preserved.
- Does not overstate beyond the deck (e.g. no performance claims). Still grounded in `Lec4.pdf`.

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
add one more question on %rowtype
```

### Expect

- Adds a single extra question specifically on `%ROWTYPE` (e.g. declaring `jobs%ROWTYPE`, reading
  `.min_salary`).
- Existing items are kept; only one is added, consistent with the current student (no-answers) state
  so it does not leak an answer.
- Still grounded in `Lec4.pdf`.

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
confirm which file this is from
```

### Expect

- Names `Lec4.pdf` (`SELECT INTO` / `%TYPE` / `%ROWTYPE`) as the source used throughout.
- Does not claim a lecture that was never selected, and does not hedge that it had no source.

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
