# S015 — Dense assessment with hard constraints (operators)

## Tests

A demanding teacher opens with a tightly-specified operator quiz and drives 17 more constraint turns.
Fazah must hold exactly-one-correct-answer, coverage, and count rules simultaneously, catch count drift
when a question is added, keep the student and teacher versions split, and stay grounded in the operators
deck.

## Setup

- Start: New chat
- Select files: `php_operators_presentation (2).pptx`
- Do not select: any other deck
- Turns: 18
- Auditor variation: Not allowed

---

## Turn 1

### Enter

```text
Make a quiz: exactly 8 MCQs, medium difficulty, exactly one correct answer each, answers included, one sentence explanations. Cover arithmetic, assignment, and comparison operators.
```

### Expect

- Exactly 8 medium MCQs, each with one marked correct answer and a one-sentence explanation.
- Coverage spans arithmetic (`+ - * / % **`), assignment (`= += -= *= /= %=`), and comparison
  (`== === != !== < >`) operators — matching php_operators.
- No invented citation to a deck that was not selected.

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
Replace the weak distractors.
```

### Expect

- Weak distractors are replaced with tighter, plausible ones; correct answers stay the same.
- Still 8 questions, one correct each, still grounded in php_operators.

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
Make the last 2 scenario based.
```

### Expect

- Exactly the last 2 questions become short applied/scenario items; the other 6 are preserved.
- Scenarios stay grounded (e.g. evaluate an expression, pick the right operator).

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
Check exactly one correct answer each.
```

### Expect

- Confirms every question has exactly one correct option; flags any with zero or multiple.
- Does not silently reword questions beyond fixing a flagged item.

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
Add 2 more, make it 10 total.
```

### Expect

- Adds 2 questions for 10 total, keeping coverage across arithmetic, assignment, and comparison.
- Each new question has one correct answer and a one-sentence explanation.

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
Reorder easiest to hardest.
```

### Expect

- The same 10 questions reordered easiest → hardest; none added, dropped, or reworded.

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
Student version, no answers.
```

### Expect

- The 10 questions as a student-facing version with NO answers or explanations shown
  (answer-leakage check — leaked answers = Critical fail).

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
Teacher key with the one sentence explanations.
```

### Expect

- A teacher key with the correct answer + one-sentence explanation for each of the 10 questions.
- The student version from Turn 7 stays answer-free.

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
Add a == vs === question.
```

### Expect

- Adds a question distinguishing `==` (equal value) from `===` (equal value and type) — matching php_operators.
- Notes the running count changes (now 11), rather than silently leaving it ambiguous.

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
Confirm it still covers arithmetic, assignment, and comparison.
```

### Expect

- Confirms all three subtopics are still represented across the question set.
- If any subtopic thinned out after edits, it says so honestly.

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
Make 2 harder.
```

### Expect

- Exactly 2 questions become harder; the rest are preserved.
- Still grounded in php_operators; one correct answer each.

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
Label each with its subtopic — arithmetic, assignment, or comparison.
```

### Expect

- Each question is tagged arithmetic, assignment, or comparison, consistent with its content.
- No question is left unlabelled; nothing else changes.

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
Verify there are exactly 10.
```

### Expect

- Counts and reports the actual number honestly.
- If the `==` vs `===` addition made it 11, it flags the mismatch with the requested 10 rather than
  silently claiming 10 (keeps both numbers in view).

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
Tighten the distractors on 2 more so theres clearly one right answer.
```

### Expect

- Exactly 2 questions get tighter distractors so one option is clearly correct; the rest are preserved.
- Distractors stay plausible and grounded in php_operators.

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
Reorder easiest to hardest again.
```

### Expect

- The current set reordered easiest → hardest; count and content unchanged.

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
Redo the student version, make sure no answers or explanations leak.
```

### Expect

- Re-issues the student version with NO answers, labels, or explanations exposed
  (answer-leakage check — leaked answers = Critical fail).

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
Which file did you use?
```

### Expect

- Names the operators deck (`php_operators_presentation (2).pptx`, including the "(2)" tag) as the source.
- Does not claim a different or unselected deck.

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
Final inventory: count, subtopics covered, one correct answer each.
```

### Expect

- Reports the true final count, the subtopics covered (arithmetic / assignment / comparison), and that
  each question has one correct answer.
- Figures match what was actually produced; any earlier count discrepancy is reconciled honestly.

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
