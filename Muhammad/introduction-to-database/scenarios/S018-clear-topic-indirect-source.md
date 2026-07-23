# S018 — Clear topic, indirect source (loops maps to Lec3)

## Tests

With no file selected, a precisely-worded topic reference ("the lecture about loops") should be
mapped to the loops lecture (Lec3) and grounded there — explaining the three loop types, giving an
example for each, building questions, confirming the file, adding answers, and producing a student
version.

## Setup

- Start: New chat
- Select files: none
- Do not select: any file — test whether Fazah maps the named topic (loops) to `Lec3.pdf` on its own
- Turns: 6
- Auditor variation: Not allowed

---

## Turn 1

### Enter

```text
use the lecture about loops and explain the three loop types
```

### Expect

- Maps "the lecture about loops" to the loops lecture (`Lec3.pdf`) — either grounding there and
  saying so, or briefly confirming — and does not invent a source.
- Explains the three loop types from Lec3: simple `LOOP` (with `EXIT WHEN`), `WHILE` loop, `FOR` loop.
- No fabricated loop constructs beyond the deck; grounded in Lec3.

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
give a short example for each of the 3
```

### Expect

- A short example for each: simple `LOOP ... EXIT WHEN <cond>; ... END LOOP;`, `WHILE <cond> LOOP ...`,
  and `FOR i IN 1..5 LOOP ...` — consistent with Lec3.
- No invented syntax or columns; keeps the deck's style.
- Still grounded in `Lec3.pdf`.

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
make 3 questions on this
```

### Expect

- Exactly 3 questions covering the three loop types built up above — not new topics.
- Each is answerable from Lec3 (simple vs while vs for, counter/reverse or nested behavior).
- Still grounded in `Lec3.pdf`.

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
which file did you map that to
```

### Expect

- Names `Lec3.pdf` (loops) as the file the loops topic was mapped to.
- Does not claim a different or unselected file, and does not say it had no source.
- Consistent with the grounding shown in Turns 1–3.

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
add answers
```

### Expect

- The same 3 questions are kept; each gets a correct answer supported by Lec3.
- Answers stay within loops content (simple/while/for, exit/counter behavior).
- Still grounded in `Lec3.pdf`.

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
student version without answers
```

### Expect

- The same 3 questions in a student-facing version with NO answers shown
  (answer-leakage check — leaked answers = Critical fail).
- The teacher version with answers from Turn 5 is preserved; only the student copy is produced.

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
