# S023 — PL/SQL data types, direct list then build-out

## Tests

With only the intro lecture selected, Fazah lists the PL/SQL data types grounded in that file, then
sustains a multi-turn build — a one-line use per type, a table, and teacher then student questions —
all grounded in Lec1.

## Setup

- Start: New chat
- Select files: `Lec1.pdf` (intro: blocks, variables, data types, scope)
- Do not select: any other lecture
- Turns: 6
- Auditor variation: Not allowed

---

## Turn 1

### Enter

```text
what are the pl/sql data types
```

### Expect

- Names the deck's types: `NUMBER`, `VARCHAR2`/`CHAR`, `Boolean`, `DATE`, `LOB` — matching Lec1.
- Grounded in the selected lecture (grounding badge / Lec1 under used sources), not a generic web list.
- Does not invent extra types (e.g. `PLS_INTEGER`, `TIMESTAMP`) as if they came from Lec1.

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
ok give a one line use for each
```

### Expect

- One short use per type: `NUMBER` = numbers (precision, scale) · `VARCHAR2`/`CHAR` = text ·
  `Boolean` = logical / true-false · `DATE` = date & time · `LOB` = images/audio/video — per Lec1.
- Reuses the same 5 types from Turn 1, not a new set.
- Still grounded in `Lec1.pdf`.

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
now put it in a table
```

### Expect

- A table pairing each of the 5 types with its one-line use from Turns 1–2.
- No new types added and no content changed — only reformatted.
- Still grounded in `Lec1.pdf`.

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
make 4 questions from this w answers
```

### Expect

- Exactly 4 questions drawn from the data-type material above, not new topics.
- Each has a correct answer supported by Lec1 (e.g. `LOB` for video, `DATE` for date/time).
- Still grounded in `Lec1.pdf`.

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

- The same 4 questions, student-facing, with NO answers shown
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
which file did this come from
```

### Expect

- Names `Lec1.pdf` (the intro / data-types lecture) as the source used throughout.
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
