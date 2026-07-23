# S027 — Explicit cursor lifecycle & attributes, quiz with traces

## Tests

With only the explicit-cursor lecture selected, Fazah explains the four-step lifecycle with the
`%found`/`%notfound`/`%rowcount` attributes, adds the cursor FOR loop, then builds a 5-question quiz —
two of them trace/scenario based — into a teacher key and a clean student version, all grounded in Lec5.

## Setup

- Start: New chat
- Select files: `Lec5.pdf` (explicit cursors)
- Do not select: any other lecture
- Turns: 7
- Auditor variation: Not allowed

---

## Turn 1

### Enter

```text
explain the explicit cursor lifecycle - declare/open/fetch/close - and give an example of %found %notfound and %rowcount
```

### Expect

- Names the four steps: `DECLARE` → `OPEN` → `FETCH ... INTO` → `CLOSE` — per Lec5.
- `%FOUND` = a row was fetched; `%NOTFOUND` = no more rows; `%ROWCOUNT` = rows fetched so far, shown
  with a short example (e.g. `EXIT WHEN emp_cur%NOTFOUND`).
- Grounded in the selected lecture (grounding badge / Lec5 under used sources); uses the deck's
  employees columns, no fabricated tables.

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
add the cursor for loop as a shorter alternative
```

### Expect

- Adds the cursor FOR loop (`FOR emp_rec IN emp_cur LOOP ...`), noting it opens/fetches/closes
  automatically — per Lec5.
- Keeps the four-step explanation; extends rather than rewrites.
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
make 5 questions across these
```

### Expect

- Exactly 5 questions spanning the lifecycle, the attributes, and the FOR loop from above — not new
  topics.
- Items are answerable from Lec5; no content invented beyond the deck.
- Still grounded in `Lec5.pdf`.

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
make 2 of them trace / scenario based
```

### Expect

- Revises so 2 of the 5 are trace/scenario questions (e.g. what `%ROWCOUNT` shows after N fetches; what
  a loop prints), in PL/SQL trace style consistent with Lec5's HR data.
- Still 5 questions total; the other 3 unchanged in intent.
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
now add answers
```

### Expect

- Adds correct answers to all 5 questions, supported by Lec5 (including the 2 trace answers).
- The same 5 questions; a teacher-facing key.
- Still grounded in `Lec5.pdf`.

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

- The same 5 questions, student-facing, with NO answers shown
  (answer-leakage check — leaked answers = Critical fail).
- The teacher key from Turn 5 is preserved; only the student copy is produced.

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
confirm which file
```

### Expect

- Names `Lec5.pdf` (explicit cursors) as the source used throughout.
- Does not claim a lecture that was never selected (e.g. the implicit-cursor `Lec5_1.pdf`), and does
  not hedge that it had no source.

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
