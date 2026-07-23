# S026 — Variable vs CONSTANT vs NOT NULL vs DEFAULT

## Tests

With only the intro lecture selected, Fazah distinguishes a normal variable, a `CONSTANT`, a `NOT NULL`
variable, and `DEFAULT`, then builds tiny examples, a table, and teacher then student questions — one
per concept — all grounded in Lec1.

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
give a concise structured explanation distinguishing a normal variable, a constant, a not null variable, and using default
```

### Expect

- Normal variable = `name datatype := value;` (can be reassigned); `CONSTANT` = must have an initial
  value and cannot be changed; `NOT NULL` = must be given an initial value; `DEFAULT` = an alternative
  to `:=` for assigning a value (`:=` ≡ `DEFAULT`) — per Lec1.
- Structured (one point per concept), grounded in Lec1.pdf (grounding badge / Lec1 under used sources).
- No invented rules beyond the deck.

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
ok give a tiny example of each
```

### Expect

- Small examples in Lec1's style, e.g. `msg varchar2(30) := 'welcome...';` (variable);
  `n constant number(2) := 5;` (`CONSTANT`); a `NOT NULL` variable with an initial value; a `DEFAULT`
  assignment.
- The same 4 concepts as Turn 1; no new ones.
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
put it in a table
```

### Expect

- A table with the 4 concepts, each with its rule and a tiny example from Turns 1–2.
- No content changed; only reformatted.
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
make 4 questions, one per concept, w answers
```

### Expect

- Exactly 4 questions — one each on variable, `CONSTANT`, `NOT NULL`, `DEFAULT`.
- Each has a correct answer supported by Lec1 (`CONSTANT` needs an initial value and can't change;
  `NOT NULL` needs an initial value; `DEFAULT` ≡ `:=`).
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
confirm which file this is from
```

### Expect

- Names `Lec1.pdf` (the intro / variables lecture) as the source used throughout.
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
