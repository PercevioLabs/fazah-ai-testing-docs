# S029 — Ten-question conditionals quiz

## Tests

With only the conditionals lecture selected, Fazah builds a fixed ten-question IF/CASE quiz, then
survives a chain of iterative edits — reorder, reshape, de-duplicate, quality-check, split into
student and teacher versions, and extend — without ever losing the ten core questions or leaking
answers into the student copy.

## Setup

- Start: New chat
- Select files: `Lec2.pdf` (IF / CASE)
- Do not select: any other lecture
- Turns: 9
- Auditor variation: Not allowed

---

## Turn 1

### Enter

```text
make me exactly 10 qs on conditionals (if/case) w answers
```

### Expect

- Exactly 10 questions on conditionals drawn from Lec2 (`IF` / `IF..ELSE` / `IF..ELSIF` / nested
  `IF` / `CASE` / searched `CASE`), each with an answer.
- Content is grounded in Lec2 (grade-band classifier, `end if;` / `end case;`); no loops or cursor
  material bleeds in.
- Grounding badge / `Lec2.pdf` under used sources; no invented citation.

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
reorder em easiest to hardest, dont change the content
```

### Expect

- New artifact version: the same 10 questions, reordered easiest → hardest.
- Question text and answers are unchanged — only the order differs (nothing rewritten or dropped).
- Still exactly 10 questions, still grounded in `Lec2.pdf`.

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
make the last 3 trace the output ones
```

### Expect

- Only the last 3 questions become trace-the-output style (given an IF/CASE block, state what it
  prints), consistent with Lec2 constructs.
- The first 7 questions are preserved unchanged; still 10 total.
- Traces are correct for Lec2 syntax; no fabricated output behavior.

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
replace any duplicate q
```

### Expect

- Any duplicate question is swapped for a distinct Lec2 conditionals question; non-duplicates left
  untouched.
- Still exactly 10 questions, each with an answer.
- If there were no duplicates, Fazah says so rather than inventing a change.

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
check each one has exactly 1 correct answer
```

### Expect

- Confirms each of the 10 has exactly one correct answer (flags/fixes any with none or with more
  than one).
- Does not silently drop or rewrite questions beyond fixing a flagged single-answer issue.
- The check is reported honestly; still 10 questions, grounded in Lec2.

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

- A student-facing version of the 10 questions with NO answers shown
  (answer-leakage check — leaked answers = Critical fail).
- The teacher version with answers is preserved separately; still 10 questions.

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
teacher key w explanations
```

### Expect

- A teacher key: the 10 questions with correct answers plus a short explanation each, grounded in
  Lec2.
- Explanations reference Lec2 constructs correctly (no fabricated rules).
- The student version from Turn 6 stays answer-free.

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
add a 3 q bonus section on searched case
```

### Expect

- A separate 3-question bonus section on searched `CASE` (`CASE WHEN grade = 'A' THEN ...`) is added,
  not replacing the 10 core questions.
- The 10 core questions remain intact; the bonus is clearly labeled/separate.
- Bonus content is grounded in Lec2's searched-CASE material.

### Record

- Actual prompt entered:
- Files selected:
- Files Fazah used:
- Result: Pass / Small Issue / Fail / Critical Fail
- Short note:

---

## Turn 9  (continue the same chat)

### Enter

```text
are the 10 core qs still there? and which file did u use
```

### Expect

- Confirms the 10 core questions are still present (now alongside the 3-question bonus).
- Names `Lec2.pdf` as the source used throughout.
- Does not claim an unselected lecture or hedge that it had no source.

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
