# S028 — SQL cursor attributes, implicit-vs-explicit synthesis

## Tests

With only the implicit-cursor lecture selected, Fazah names the `SQL%` cursor attributes, explains
their behaviour after DML, contrasts implicit vs explicit cursors into a table and quick-check
questions, then confirms the source — all grounded in Lec5_1 without claiming the unselected
explicit-cursor file.

## Setup

- Start: New chat
- Select files: `Lec5_1.pdf` (implicit cursors & SQL cursor attributes)
- Do not select: any other lecture
- Turns: 9
- Auditor variation: Not allowed

---

## Turn 1

### Enter

```text
what are the sql cursor attributes
```

### Expect

- Names `SQL%FOUND`, `SQL%NOTFOUND`, `SQL%ROWCOUNT`, `SQL%ISOPEN` — per Lec5_1.
- Notes these belong to the implicit (`SQL`) cursor.
- Grounded in the selected lecture (grounding badge / Lec5_1 under used sources), not a generic answer.

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
how do they work after an update or delete
```

### Expect

- `SQL%FOUND` = TRUE if the DML affected ≥1 row; `SQL%NOTFOUND` = TRUE if 0 rows; `SQL%ROWCOUNT` =
  number of rows affected; `SQL%ISOPEN` = always FALSE (Oracle closes the implicit cursor) — per Lec5_1.
- Ties to UPDATE/DELETE (rows affected), consistent with the deck's STUDENT/`UPDATE` example.
- Still grounded in `Lec5_1.pdf`.

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
how is an implicit cursor different from an explicit one
```

### Expect

- Implicit (`SQL`) cursor is opened automatically for INSERT/UPDATE/DELETE/`SELECT INTO`; an explicit
  cursor is declared by the programmer for a multi-row SELECT (DECLARE/OPEN/FETCH/CLOSE).
- Notes `SQL%ISOPEN` is always FALSE for the implicit cursor; explicit is programmer-managed.
- Grounded in `Lec5_1.pdf`; keeps the explicit contrast at the overview level and does not fabricate
  deep explicit-cursor detail from a file that was not selected.

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
put implicit vs explicit in a compact table
```

### Expect

- A compact table: who opens it (Oracle vs programmer), used for (DML/`SELECT INTO` vs multi-row
  SELECT), lifecycle (automatic vs DECLARE/OPEN/FETCH/CLOSE), `%ISOPEN` (always FALSE vs managed).
- Built from Turn 3; no new claims.
- Still grounded in `Lec5_1.pdf`.

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
turn that table into 3 student quick-check qs
```

### Expect

- Exactly 3 quick-check questions drawn from the implicit-vs-explicit table, not new topics.
- Items are answerable from the material above.
- Still grounded in `Lec5_1.pdf`.

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
add a teacher key for those
```

### Expect

- An answer key for the same 3 questions (keeps the set, adds correct answers).
- Each answer is supported by Lec5_1 (implicit auto-opened; `SQL%ISOPEN` FALSE; explicit declared).
- Still grounded in `Lec5_1.pdf`.

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
student version, no answers
```

### Expect

- The same 3 questions, student-facing, with NO answers shown
  (answer-leakage check — leaked answers = Critical fail).
- The teacher key from Turn 6 is preserved; only the student copy is produced.

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
add one q on sql%rowcount
```

### Expect

- Adds one more question specifically on `SQL%ROWCOUNT` (number of rows affected by the DML) — per Lec5_1.
- The existing 3 items are kept; only one is added, consistent with the current student (no-answers)
  state so it does not leak an answer.
- Still grounded in `Lec5_1.pdf`.

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
confirm all of this came from the implicit-cursor lecture
```

### Expect

- Confirms the source is the implicit-cursor lecture (`Lec5_1.pdf`), the file that was selected.
- Does not claim the explicit-cursor lecture (`Lec5.pdf`) or any other unselected file.
- If the earlier explicit-cursor contrast leaned on general knowledge, it is honest about which file
  backed it (no fabricated citation).

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
