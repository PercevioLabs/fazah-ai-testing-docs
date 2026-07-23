# S007 — Explicit selection overrides chat history

## Tests

After a procedures answer (Lec6), the auditor explicitly switches to the loops lecture (Lec3); Fazah
follows the new selection instead of the earlier topic, stays on the loops file through follow-ups,
names it as the source, and produces reordered teacher and student questions from it.

## Setup

- Start: New chat
- Select files: `Lec6.pdf` (procedures & functions)
- Do not select: any other lecture yet (`Lec3.pdf` is selected at Turn 2)
- Turns: 7
- Auditor variation: Not allowed

---

## Turn 1

### Enter

```text
explain what a procedure is
```

### Expect

- Procedure = a subprogram that performs tasks; parameter modes `IN` / `OUT` / `IN OUT`;
  `CREATE [OR REPLACE] PROCEDURE` — matching Lec6.
- Grounded in `Lec6.pdf`.
- No fabricated verbatim example (Lec6's worked examples are image slides).

### Record

- Actual prompt entered:
- Files selected:
- Files Fazah used:
- Result: Pass / Small Issue / Fail / Critical Fail
- Short note:

---

## Turn 2  (continue the same chat — deselect `Lec6.pdf`, select `Lec3.pdf`)

### Enter

```text
now explain the for loop
```

### Expect

- Uses the newly selected loops file (Lec3): `FOR i IN 1..5 LOOP`; `REVERSE` counts down.
- The explicit selection overrides the procedures history — grounds in Lec3, not Lec6.
- No loop content misattributed to Lec6.

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
keep using the loops file — whats the difference between while and simple loop
```

### Expect

- `WHILE` checks the condition first; simple `LOOP` runs then exits via `EXIT WHEN` — per Lec3.
- Stays on the loops file (Lec3).

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
make 5 questions from the loops file
```

### Expect

- Exactly five questions grounded in Lec3 (simple/while/for, reverse, nested).
- No procedures / Lec6 content.

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
which file are these from
```

### Expect

- Names the loops lecture (`Lec3.pdf`) as the source.
- Not Lec6; no invented citation.

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
reorder them easy to hard
```

### Expect

- The same five questions reordered from easiest to hardest; content unchanged.
- Still grounded in Lec3.

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
now a student version
```

### Expect

- A student-facing version of the five questions with NO answers shown
  (answer-leakage check — leaked answers = Critical fail).
- The order and content from Turn 6 are preserved.

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
