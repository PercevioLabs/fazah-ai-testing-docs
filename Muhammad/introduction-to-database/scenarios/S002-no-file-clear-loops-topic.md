# S002 — No file selected, clear loops topic

## Tests

With no file selected, Fazah auto-selects the right lecture for a clearly-scoped loops question, then
sustains a multi-turn workflow — deepening it, tabulating, naming its source, and turning it into
teacher and student review — all grounded in the loops lecture (Lec3).

## Setup

- Start: New chat
- Select files: none — leave the file picker empty
- Do not select: any file (Fazah must auto-select)
- Turns: 6
- Auditor variation: Not allowed

---

## Turn 1

### Enter

```text
can u explain simple loop, while loop and for loop
```

### Expect

- Explains all three forms: simple `LOOP` with `EXIT WHEN`, `WHILE` (checks the condition first),
  `FOR i IN 1..5 LOOP` — matching Lec3.
- With no file selected, Fazah auto-selects and grounds in the loops lecture (Lec3), not a generic
  web answer.
- No loop constructs invented beyond the deck.

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
ok go deeper on the for loop — what does reverse actually do
```

### Expect

- Explains `FOR i IN REVERSE 1..5 LOOP` counts down instead of up (reverse/counter behavior) per Lec3.
- Keeps the Turn 1 explanation and extends it, not a rewrite.
- Still grounded in the loops lecture (Lec3).

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
now compare while vs for in a table
```

### Expect

- A table contrasting `WHILE` (condition-first, runs while true) and `FOR` (fixed range `1..5`) per
  Lec3.
- Facts consistent with the deck; nothing invented.
- Still grounded in the loops lecture.

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
which lecture did this come from
```

### Expect

- Names the loops lecture (Lec3) as the source it auto-selected.
- Does not claim a file that was never available, and does not hedge that it had no source.

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
make 3 review qs w answers
```

### Expect

- Exactly three questions on the loop material built up above (simple/while/for, reverse) with correct
  answers supported by Lec3.
- Not new topics.
- Still grounded in the loops lecture.

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
now a student version, no answers
```

### Expect

- The same three questions in a student-facing version with NO answers shown
  (answer-leakage check — leaked answers = Critical fail).
- The teacher version from Turn 5 is preserved; only the student copy is produced.

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
