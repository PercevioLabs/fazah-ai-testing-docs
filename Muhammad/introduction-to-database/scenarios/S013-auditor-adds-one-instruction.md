# S013 — Auditor adds one instruction, block structure

## Tests

With the intro lecture selected, Fazah explains the PL/SQL block structure while honoring one extra
instruction the auditor adds, then carries the work through examples, a student summary, and a check —
all grounded in Lec1.

## Setup

- Start: New chat
- Select files: `Lec1.pdf` (intro: blocks, variables, data types, scope)
- Do not select: any other lecture
- Turns: 6
- Auditor variation: Allowed — see the Auditor variation section

---

## Turn 1

### Enter

```text
explain the PL/SQL block structure (declarative, executable, exception)
```

(Then add exactly one instruction — see the Auditor variation section.)

### Expect

- Names the three parts: Declarative (optional), Executable (mandatory, between `BEGIN` and `END`),
  Exception (optional) — per Lec1.
- Honors the one added instruction (e.g. a table / an example / audience / length) without dropping the
  block-structure explanation.
- Grounded in `Lec1.pdf`; no fabricated citation.

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
add a tiny example for each section
```

### Expect

- A small example for each of Declarative / Executable / Exception, in Lec1 style (a variable
  declaration; `dbms_output.put_line(...)` inside `begin ... end;`; an exception section).
- The prior explanation is preserved.

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
turn it into a short student summary
```

### Expect

- A concise student-facing summary of the block structure.
- Content grounded in Lec1; no fabricated facts.

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
make a 3 question check
```

### Expect

- Exactly 3 questions on the block structure.
- Answerable from Lec1; no fabricated content.

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
student version, no answers
```

### Expect

- The same 3 questions, student-facing, with NO answers shown
  (answer-leakage check — leaked answers = Critical fail).
- The teacher content is preserved.

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
which file did you use
```

### Expect

- Names `Lec1.pdf` (intro / block structure) as the source used.
- Does not claim a lecture that was never selected.

### Record

- Actual prompt entered:
- Files selected:
- Files Fazah used:
- Result: Pass / Small Issue / Fail / Critical Fail
- Short note:

---

## Auditor variation

Add or change one realistic instruction. Record exactly what you entered. Do not change the scenario's
main goal.

Examples:
- present it as a table
- add one worked example
- write it for first-year students
- keep it under 200 words

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
