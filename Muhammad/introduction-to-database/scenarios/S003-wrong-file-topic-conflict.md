# S003 — Wrong file selected, topic conflict

## Tests

The wrong lecture is selected for a cursor question (conditionals, Lec2); Fazah flags the mismatch
honestly without fabricating, guides the user to the right file, then — once Lec5 is selected —
delivers the explicit-cursor material as teacher and student assessment grounded in the corrected file.

## Setup

- Start: New chat
- Select files: `Lec2.pdf` (IF / CASE) — deliberately wrong for the ask
- Do not select: `Lec5.pdf` yet (it is selected at Turn 3)
- Turns: 8
- Auditor variation: Not allowed

---

## Turn 1

### Enter

```text
explain explicit cursors from the selected slides
```

### Expect

- Recognizes the selected file (Lec2, IF/CASE) does not cover explicit cursors and flags the mismatch
  honestly.
- Does NOT fabricate cursor content and attribute it to Lec2.
- Either asks for the cursor lecture or states the selected file lacks that topic.

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
so which file shd i use for cursors then
```

### Expect

- Points to the explicit-cursor lecture (Lec5) as the correct source for cursors.
- Does not pretend Lec2 covers cursors.

### Record

- Actual prompt entered:
- Files selected:
- Files Fazah used:
- Result: Pass / Small Issue / Fail / Critical Fail
- Short note:

---

## Turn 3  (continue the same chat — select `Lec5.pdf`)

### Enter

```text
ok use this cursor lecture instead
```

### Expect

- Switches its grounding source to the newly selected Lec5 (explicit cursors).
- Acknowledges the corrected file rather than staying on Lec2.

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
now explain the 4 steps to use an explicit cursor properly
```

### Expect

- Names the four steps: `DECLARE` the cursor → `OPEN` → `FETCH ... INTO` → `CLOSE` — matching Lec5.
- Grounded in `Lec5.pdf`, not Lec2.

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
gimme a short example that fetches employees in a loop
```

### Expect

- A short explicit-cursor example that OPENs, FETCHes in a loop with `EXIT WHEN emp_cur%NOTFOUND`, and
  CLOSEs — consistent with Lec5's `employees` example (`employee_id`, `last_name`, `salary`).
- No fabricated columns/tables.

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
put those 4 steps in a table
```

### Expect

- A table of the four steps (`DECLARE` / `OPEN` / `FETCH ... INTO` / `CLOSE`), consistent with the
  prior answer.
- Still grounded in `Lec5.pdf`.

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
make 5 student qs, no answers
```

### Expect

- Exactly five student-facing questions on explicit cursors with NO answers shown
  (answer-leakage check — leaked answers = Critical fail).
- Grounded in `Lec5.pdf`.

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
which file did you end up using for these
```

### Expect

- Names the explicit-cursor lecture (`Lec5.pdf`) as the source used, not Lec2.
- Honest about the source switch; no invented citation.

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
