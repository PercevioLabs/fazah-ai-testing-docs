# S016 — Informal refinement language, exceptions (thin lecture)

## Tests

With no file selected, Fazah explains exception handling and refines it through informal follow-ups
(simpler, an analogy, a 4-line summary, questions, a student version) — staying strictly at the thin
Lec7 depth and never fabricating deeper exception content.

## Setup

- Start: New chat
- Select files: none
- Do not select: any lecture (exceptions is Lec7 content, but nothing is selected)
- Turns: 7
- Auditor variation: Allowed — see the Auditor variation section

> Lec7 is thin (image slides). Only these are supported: `NO_DATA_FOUND` (query returns no rows),
> `TOO_MANY_ROWS` (query returns more than one row), `OTHERS` (catch-all), and the `EXCEPTION` section.
> Fazah must NOT fabricate deeper content (`RAISE`, user-defined exceptions, `SQLERRM`/`SQLCODE`).

---

## Turn 1

### Enter

```text
explain exception handling in PL/SQL
```

### Expect

- Explains that the `EXCEPTION` section handles errors, and names `NO_DATA_FOUND` (no rows),
  `TOO_MANY_ROWS` (more than one row), and `OTHERS` (catch-all) — at Lec7 level.
- Does NOT fabricate deeper content (`RAISE`, user-defined exceptions, `SQLERRM`/`SQLCODE`) — staying
  at this depth is the correct behavior.
- No file is selected, so no invented citation.

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
make it way simpler
```

### Expect

- Simplifies the same explanation while keeping the three exceptions accurate.
- Does not add deeper fabricated exception content while "simplifying".

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
give a real classroom analogy but dont change the definition
```

### Expect

- Adds a plain classroom analogy; the technical definition of the `EXCEPTION` section and the three
  exceptions is unchanged.
- Still no fabricated deeper content.

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
make it a 4 line summary
```

### Expect

- A 4-line summary of exception handling at Lec7 depth.
- Accurate and concise; the three exceptions preserved.

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
add 3 quick qs
```

### Expect

- Exactly 3 questions on the `EXCEPTION` section / the three named exceptions.
- Answerable at Lec7 level; no fabricated exception types in the questions.

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
keep the definition but give me a student version
```

### Expect

- A student-facing version with the definition preserved.
- If the 3 questions are included, no answers are leaked (answer-leakage check — leaked answers =
  Critical fail).

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
what lecture is this
```

### Expect

- Honest about source: no lecture was selected (this maps to the exceptions lecture — Lec7 — but was
  not grounded in a selected file).
- Does NOT claim it used a selected lecture when none was selected.

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
- make it even shorter
- change the analogy's domain (e.g. sports)
- add one small example
- ask for a single paragraph

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
