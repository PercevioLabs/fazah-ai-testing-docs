# S004 — Two files, structured comparison

## Tests

With conditionals (Lec2) and loops (Lec3) both selected, Fazah builds a structured comparison table
scoped only to those two files, then iterates on it — adding rows and code, condensing, and producing
teacher and student assessment — without pulling in any unselected lecture.

## Setup

- Start: New chat
- Select files: `Lec2.pdf` (IF / CASE) and `Lec3.pdf` (loops)
- Do not select: any other lecture
- Turns: 7
- Auditor variation: Not allowed

---

## Turn 1

### Enter

```text
compare conditional statements (if/case) and loops in a table — when to use each + 1 example each, use only the selected slides
```

### Expect

- A table contrasting conditionals (IF/CASE, Lec2) and loops (Lec3), with a when-to-use cell and one
  example each.
- Grounded only in the two selected lectures; no content from any other file.
- Examples consistent with the decks (grade bands / `FOR i IN 1..5`).

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
add a row for general syntax
```

### Expect

- Adds a syntax row (e.g. `if..then..end if` / `CASE...END CASE` vs `LOOP...END LOOP` /
  `WHILE...LOOP` / `FOR i IN 1..5 LOOP`) per the decks.
- Keeps the existing table content, not a rewrite.

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
now add one short code example per row
```

### Expect

- One short code snippet per row, consistent with Lec2 (grade classifier) and Lec3 (a loop).
- No fabricated constructs or columns.
- Still scoped to the two selected files.

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
condense all this to a one-slide summary
```

### Expect

- A compact one-slide summary of the comparison; facts kept, detail trimmed.
- Still only Lec2 and Lec3 content.

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
make 4 quiz qs w answers
```

### Expect

- Exactly four questions across conditionals and loops with correct answers grounded in Lec2/Lec3.
- No topics outside the two selected files.

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

- The same four questions in a student-facing version with NO answers shown
  (answer-leakage check — leaked answers = Critical fail).
- The teacher version from Turn 5 is preserved.

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
confirm you only used the two selected lectures
```

### Expect

- Confirms only Lec2 and Lec3 were used throughout.
- Does not cite any unselected file, and does not claim a broader source.

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
