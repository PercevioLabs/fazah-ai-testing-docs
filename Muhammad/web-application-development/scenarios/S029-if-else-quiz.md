# S029 — If/elseif/else quiz, long iterative build

## Tests

With only the if_else deck selected, Fazah builds a 10-question if/elseif/else quiz and then sustains
a long iterative refinement — reorder, trace-output, dedupe, bonus and scenario items, subtopic
labels, harder items, and finally split student/teacher deliverables — all grounded in the same deck,
preserving every count and never leaking answers into a student version.

## Setup

- Start: New chat
- Select files: `php_if_else_presentation.pptx`
- Do not select: any other deck
- Turns: 18
- Auditor variation: Not allowed

---

## Turn 1

### Enter

```text
make me exactly 10 quiz qs on if / elseif / else w/ answers
```

### Expect

- Produces exactly 10 questions on if / elseif / else, each with a correct answer.
- Covers `if`, `if…else`, and `if…elseif…else` (the deck's structures), not unrelated topics.
- Grounded in the selected if_else deck; no citation to an unselected deck.

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
reorder them easiest to hardest, dont change any wording
```

### Expect

- Same 10 questions reordered easiest → hardest; wording and content unchanged.
- None added or dropped; still 10, still php_if_else.

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
make the last 3 trace-the-output ones
```

### Expect

- Only the last 3 become trace-the-output questions; the first 7 are unchanged.
- Traced code is valid PHP consistent with the deck (e.g. the hour-based greeting) with correct output.
- Still 10 total.

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
if any 2 are basically the same replace one
```

### Expect

- Checks for duplicate/near-duplicate items; replaces only a duplicate with a distinct if/elseif/else question.
- Count stays 10; the other questions are preserved.

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

- Confirms each of the 10 has exactly one correct answer (none with multiple-correct or none-correct).
- Fixes any that fail without silently altering the others.

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
ok now a student version, no answers
```

### Expect

- Same 10 questions, student-facing, with NO answers shown
  (answer-leakage check — leaked answers = Critical fail).
- Content unchanged from the 10; still grounded in php_if_else.

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
and a teacher key w short explanations
```

### Expect

- Teacher key with the correct answer + a short explanation for each of the 10, grounded in the deck.
- The student version stays answer-free.

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
add 3 bonus qs on the greeting example (the good morning / afternoon thing)
```

### Expect

- Adds exactly 3 bonus questions based on the deck's hour-based greeting example
  (`if ($time < 12)` morning / `elseif ($time < 18)` afternoon / `else` …).
- Bonus set kept separate; the 10 core remain intact.

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
the 10 core are still all there right
```

### Expect

- Confirms the 10 core questions are unchanged and still present, separate from the 3 bonus.
- No content lost across the edits.

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
add 2 scenario based qs but keep the 10 core
```

### Expect

- Adds 2 scenario-based if/elseif/else questions; the 10 core (and the 3 bonus) are preserved.
- Scenarios grounded in if/elseif/else logic from the deck.

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
label each q w/ which subtopic it tests (if / elseif / else)
```

### Expect

- Each question labelled by subtopic (`if` / `if…else` / `if…elseif…else`), matching the deck's structures.
- Labelling does not change any question content.

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
which lecture did u use for all this
```

### Expect

- Names `php_if_else_presentation.pptx` as the source used throughout.
- Does not claim an unselected deck and does not hedge that it had no source.

### Record

- Actual prompt entered:
- Files selected:
- Files Fazah used:
- Result: Pass / Small Issue / Fail / Critical Fail
- Short note:

---

## Turn 13  (continue the same chat)

### Enter

```text
make 2 of the core ones harder
```

### Expect

- Exactly 2 of the 10 core become harder; the rest are preserved. Bonus and scenario items untouched.
- Still grounded; still exactly 10 core.

### Record

- Actual prompt entered:
- Files selected:
- Files Fazah used:
- Result: Pass / Small Issue / Fail / Critical Fail
- Short note:

---

## Turn 14  (continue the same chat)

### Enter

```text
how many qs total now, break it down
```

### Expect

- Reports an accurate breakdown: 10 core + 3 bonus + 2 scenario = 15 total.
- Numbers consistent with the running edits; nothing silently dropped.

### Record

- Actual prompt entered:
- Files selected:
- Files Fazah used:
- Result: Pass / Small Issue / Fail / Critical Fail
- Short note:

---

## Turn 15  (continue the same chat)

### Enter

```text
reorder the 10 core easiest to hardest again
```

### Expect

- The 10 core reordered easiest → hardest; content unchanged; bonus and scenario sets unaffected.
- Still 10 core.

### Record

- Actual prompt entered:
- Files selected:
- Files Fazah used:
- Result: Pass / Small Issue / Fail / Critical Fail
- Short note:

---

## Turn 16  (continue the same chat)

### Enter

```text
regen the student version, make sure no answers show
```

### Expect

- Updated student version reflecting all edits, with NO answers
  (answer-leakage check — leaked answers = Critical fail).
- Includes the current question set; teacher key kept separate.

### Record

- Actual prompt entered:
- Files selected:
- Files Fazah used:
- Result: Pass / Small Issue / Fail / Critical Fail
- Short note:

---

## Turn 17  (continue the same chat)

### Enter

```text
give me an inventory of everything we made
```

### Expect

- Lists all assets: 10 core, 3 bonus, 2 scenario, student version (no answers), teacher key — with counts.
- Matches what was actually produced; no invented items.

### Record

- Actual prompt entered:
- Files selected:
- Files Fazah used:
- Result: Pass / Small Issue / Fail / Critical Fail
- Short note:

---

## Turn 18  (continue the same chat)

### Enter

```text
ok final — give me 2 separate docs, student sheet no answers + teacher key
```

### Expect

- Delivers two separate deliverables: a student sheet with NO answers and a teacher key with
  answers/explanations (answer-leakage check — leaked answers = Critical fail).
- Both consistent with the final question set; nothing merged or leaked.

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
