# S001 — Selected cursor lecture, direct concept question

## Tests

With only the explicit-cursor lecture selected, Fazah answers a direct concept question grounded in
that file, then sustains a multi-turn workflow — deepening it, adding an example, and turning it into
teacher and student assessment — all grounded in the same lecture.

## Setup

- Start: New chat
- Select files: `Lec5.pdf` (explicit cursors)
- Do not select: any other lecture
- Turns: 6
- Auditor variation: Not allowed

---

## Turn 1

### Enter

```text
whats the four steps to use an explicit cursor
```

### Expect

- Names the four steps: `DECLARE` the cursor → `OPEN` → `FETCH ... INTO` → `CLOSE` — matching Lec5.
- The reply is grounded in the selected lecture (grounding badge / Lec5 under used sources), not a
  generic web answer.
- No invented citation to a lecture that was not selected.

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
ok add what the cursor attributes do — %found %notfound %rowcount
```

### Expect

- The four-step answer is kept and extended (not rewritten from scratch).
- `%FOUND` = a row was fetched; `%NOTFOUND` = no more rows; `%ROWCOUNT` = rows fetched so far — per Lec5.
- Still grounded in `Lec5.pdf`.

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
gimme a short example that fetches employees in a loop
```

### Expect

- A short explicit-cursor example that OPENs, FETCHes in a loop with `EXIT WHEN emp_cur%NOTFOUND`,
  and CLOSEs — consistent with Lec5's `employees` example.
- Uses the deck's style (`employee_id`, `last_name`, `salary`); no fabricated columns/tables.
- Still grounded in the selected lecture.

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
ok turn all this into 4 short quiz qs w answers
```

### Expect

- Exactly four questions covering the cursor material built up above (steps, attributes, the loop) —
  not new topics.
- Each question has a correct answer supported by Lec5.
- Still grounded in `Lec5.pdf`.

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
now a student version of those 4, no answers
```

### Expect

- The same four questions in a student-facing version with NO answers shown
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
which lecture did you use for all this
```

### Expect

- Names the explicit-cursor lecture (`Lec5.pdf`) as the source used throughout.
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
