# S021 — Conflicting item counts (10 vs exactly 15)

## Tests

The opening request gives two contradictory counts in one breath — "10 questions" and "exactly 15
questions". Fazah must flag the conflict instead of silently picking one, accept the teacher's
resolution to 12, then build and refine a 12-question if/else assessment grounded in `php_if_else`,
holding the count through every later edit and never leaking answers in the student version.

## Setup

- Start: New chat
- Select files: none at first; from Turn 3 select `php_if_else_presentation.pptx`
- Do not select: any other deck
- Turns: 12
- Auditor variation: Not allowed

---

## Turn 1

### Enter

```text
make 10 questions and keep the assessment to exactly 15 questions
```

### Expect

- Flags the contradiction — 10 vs "exactly 15" cannot both hold — and asks which count to use.
- Does **NOT** silently pick 10 or 15, and does not produce an assessment yet.

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
actually lets make it 12
```

### Expect

- Accepts 12 as the resolved count and confirms the earlier 10/15 conflict is settled.
- Waits for a source (nothing selected yet) rather than inventing one.

### Record

- Actual prompt entered:
- Files selected:
- Files Fazah used:
- Result: Pass / Small Issue / Fail / Critical Fail
- Short note:

---

## Turn 3  (continue the same chat — select `php_if_else_presentation.pptx`)

### Enter

```text
use this if/else deck, 12 questions
```

### Expect

- Produces exactly twelve questions grounded in `php_if_else` (`if`, `if…else`, `if…elseif…else`,
  e.g. the hour-based greeting example).
- No answers shown yet; no facts outside php_if_else.

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
add the answers
```

### Expect

- One correct answer per question, each supported by php_if_else.
- Still exactly twelve questions.

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

- The same twelve questions in a student-facing version with NO answers shown
  (answer-leakage check — leaked answers = Critical fail).

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
confirm its 12 questions
```

### Expect

- Confirms exactly twelve questions across the versions and the key.
- No content changed while confirming.

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
add a scenario q but keep it at 12
```

### Expect

- Introduces one scenario question (e.g. choose the right branch for a given `$time`) by **replacing**
  an existing one, so the count stays exactly twelve.
- Grounded in php_if_else; no drift to 13.

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
reorder easiest to hardest
```

### Expect

- The same twelve questions reordered easiest → hardest; none added or dropped, content unchanged.

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
teacher key w explanations
```

### Expect

- A teacher key with the correct answer + a short explanation for each of the twelve, grounded in php_if_else.
- The student version stays answer-free.

### Record

- Actual prompt entered:
- Files selected:
- Files Fazah used:
- Result: Pass / Small Issue / Fail / Critical Fail
- Short note:

---

## Turn 10  (continue the same chat)

### Enter

```text
make 3 of them harder
```

### Expect

- Exactly three questions become harder; the other nine are preserved. Still twelve, still grounded.

### Record

- Actual prompt entered:
- Files selected:
- Files Fazah used:
- Result: Pass / Small Issue / Fail / Critical Fail
- Short note:

---

## Turn 11  (continue the same chat)

### Enter

```text
verify the count is still 12
```

### Expect

- Confirms the assessment is still exactly twelve after the harder edits.
- Reports if any version drifted off 12 rather than glossing over it.

### Record

- Actual prompt entered:
- Files selected:
- Files Fazah used:
- Result: Pass / Small Issue / Fail / Critical Fail
- Short note:

---

## Turn 12  (continue the same chat)

### Enter

```text
inventory + which deck did u use
```

### Expect

- Lists what was built: a 12-question if/else assessment, a student version (no answers), and a teacher key.
- Names the single source: `php_if_else_presentation.pptx`.

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
