# S011 — Conversational classroom problem, no file selected

## Tests

Starting from a chatty real-classroom problem (students confusing `%TYPE` and `%ROWTYPE`) with no file
selected, Fazah explains the difference, then builds an activity, board examples, a handout, and an
exit ticket — staying at Lec4 depth and honest that no file was the source.

## Setup

- Start: New chat
- Select files: none
- Do not select: any lecture (`%TYPE` / `%ROWTYPE` is Lec4 content, but nothing is selected)
- Turns: 7
- Auditor variation: Not allowed

---

## Turn 1

### Enter

```text
my students keep mixing up %TYPE and %ROWTYPE, can u help me explain the difference before class
```

### Expect

- `%TYPE` = one variable matching a column's type (e.g. `i employees.employee_id%TYPE;`); `%ROWTYPE` =
  a record matching a whole row (e.g. `job_rec jobs%ROWTYPE;`, read via `job_rec.min_salary`) — per Lec4.
- No file is selected, so Fazah answers generally or notes nothing is selected; no invented citation.
- Uses the deck's schema style (employees / jobs); no fabricated tables or columns.

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
gimme a quick 2 min activity to check if they got it
```

### Expect

- A short 2-minute check-for-understanding activity that distinguishes `%TYPE` from `%ROWTYPE`.
- Grounded in the same concept; no fabricated schema beyond employees / jobs style.
- Builds on Turn 1 (does not restart).

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
3 quick examples of each for the board
```

### Expect

- 3 `%TYPE` examples and 3 `%ROWTYPE` examples, in Lec4 style (employees / jobs columns).
- No fabricated tables or columns.
- Consistent with the earlier explanation.

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
turn that into a short one page handout
```

### Expect

- Consolidates the explanation and examples into a short one-page handout.
- Preserves prior content; no new fabricated facts.
- Still `%TYPE` / `%ROWTYPE` at Lec4 depth.

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
add a 3 question exit ticket
```

### Expect

- Exactly 3 questions on `%TYPE` / `%ROWTYPE`.
- Answerable at Lec4 level; no fabricated content.
- Handout content preserved.

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
student version of the exit ticket, no answers
```

### Expect

- The same 3 questions, student-facing, with NO answers shown
  (answer-leakage check — leaked answers = Critical fail).
- The handout / teacher content is preserved.

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
what lecture did this come from
```

### Expect

- Honest about source: no lecture was selected (this maps to the `SELECT INTO` / `%TYPE` / `%ROWTYPE`
  lecture — Lec4 — but was not grounded in a selected file).
- Does NOT claim it used a selected lecture when none was selected.

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
