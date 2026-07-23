# S015 — Dense assessment constraints

## Tests

Fazah satisfies a dense set of assessment constraints, then sustains a demanding teacher's run of
targeted refinements — distractor swaps, scenario conversions, a consistency check, growing to ten,
reordering, student/teacher split, and a coverage confirmation — without disturbing the rest.

## Setup

- Start: New chat
- Select files: `Ch4 Testing.pptx`
- Do not select: any other deck
- Turns: 9
- Auditor variation: Not allowed

---

## Turn 1

### Enter

```text
make a quiz from the testing lecture, these rules:
- exactly 8 mcqs
- medium difficulty
- exactly 1 correct answer per q
- include the answers
- one sentence explanation for each
- cover unit, component, system, release n user testing across the set
```

### Expect

- Exactly 8 MCQs at medium difficulty, each with exactly one correct answer marked.
- Each question includes the answer and a one-sentence explanation.
- The set spans all five areas: unit, component, system, release, and user testing.
- Content is grounded in the selected Testing deck (`Ch4 Testing.pptx`).

### Record

- Actual prompt entered:
- Files selected:
- Files Fazah used:
- Result: Pass / Small Issue / Fail / Critical Fail
- Short note:

---

## Turn 2   (continue the same chat)

### Enter

```text
replace only the weakest distractors
```

### Expect

- Only weak distractors are changed; question stems and correct answers are preserved.
- Still exactly 8 MCQs (a new version of the same quiz).
- Difficulty, coverage, and explanations are unchanged.

### Record

- Actual prompt entered:
- Files selected:
- Files Fazah used:
- Result: Pass / Small Issue / Fail / Critical Fail
- Short note:

---

## Turn 3   (continue the same chat)

### Enter

```text
make the last 2 qs scenario based
```

### Expect

- Only the last two questions become scenario-based (e.g. weather station / Mentcare allergy tests).
- The other six questions are unchanged; still exactly 8 MCQs.
- Five-area coverage across the set is not broken.

### Record

- Actual prompt entered:
- Files selected:
- Files Fazah used:
- Result: Pass / Small Issue / Fail / Critical Fail
- Short note:

---

## Turn 4   (continue the same chat)

### Enter

```text
check each q still has exactly 1 correct answer
```

### Expect

- Confirms one correct answer per question across all 8.
- Flags and fixes any question with zero or multiple correct options (if any).

### Record

- Actual prompt entered:
- Files selected:
- Files Fazah used:
- Result: Pass / Small Issue / Fail / Critical Fail
- Short note:

---

## Turn 5   (continue the same chat)

### Enter

```text
add 2 more to make 10, still medium difficulty
```

### Expect

- Adds exactly two questions for a total of 10, both at medium difficulty.
- The existing eight (including the scenario-based pair) are preserved.
- One correct answer and a one-sentence explanation each for the new questions.

### Record

- Actual prompt entered:
- Files selected:
- Files Fazah used:
- Result: Pass / Small Issue / Fail / Critical Fail
- Short note:

---

## Turn 6   (continue the same chat)

### Enter

```text
reorder them easiest to hardest
```

### Expect

- Same 10 questions reordered easiest to hardest — none added or removed.
- Answers and explanations stay attached to their questions after reordering.

### Record

- Actual prompt entered:
- Files selected:
- Files Fazah used:
- Result: Pass / Small Issue / Fail / Critical Fail
- Short note:

---

## Turn 7   (continue the same chat)

### Enter

```text
gimme a student version, no answers
```

### Expect

- Produces all 10 questions with NO answers or explanations shown.
- Answer leakage into the student version = Critical fail.
- Question order from turn 6 is preserved.

### Record

- Actual prompt entered:
- Files selected:
- Files Fazah used:
- Result: Pass / Small Issue / Fail / Critical Fail
- Short note:

---

## Turn 8   (continue the same chat)

### Enter

```text
now the teacher key w explanations
```

### Expect

- Produces a separate teacher key: the same 10 questions with correct answers and explanations.
- Matches the student version item-for-item (same questions, same order).

### Record

- Actual prompt entered:
- Files selected:
- Files Fazah used:
- Result: Pass / Small Issue / Fail / Critical Fail
- Short note:

---

## Turn 9   (continue the same chat)

### Enter

```text
confirm the set still covers all 5 testing areas
```

### Expect

- Confirms coverage across unit, component, system, release, and user testing.
- Honestly flags any area that dropped out during the edits rather than claiming coverage it lost.

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
