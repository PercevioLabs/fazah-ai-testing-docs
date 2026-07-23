# S037 — MCQ quiz quality refinement and answer separation

## Tests

Over eleven turns Fazah builds a Testing MCQ quiz, self-reviews it (deduplicate, strengthen distractors,
single-correct-answer check), separates a no-answers student version from a teacher key, extends coverage
to TDD, reorders and labels subtopics, and confirms both the source and the one-correct-answer invariant.

## Setup

- Start: New chat
- Select files: `Ch4 Testing.pptx`
- Do not select: any other deck
- Turns: 11
- Auditor variation: Not allowed

---

## Turn 1

### Enter

```text
Create twelve MCQs covering the full Testing lecture.
```

### Expect

- Exactly twelve multiple-choice questions.
- Coverage spans the Testing lecture (e.g. development / release / user testing, verification vs
  validation, TDD, interface errors, partition testing).
- Grounded in `Ch4 Testing.pptx`; no invented citation.

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
Identify and replace any duplicate questions.
```

### Expect

- Any duplicate or near-duplicate questions are identified and replaced with new ones.
- Still exactly twelve MCQs.
- Non-duplicate questions are preserved.

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
Improve the weak distractors.
```

### Expect

- Weak / implausible answer options are improved so distractors are plausible.
- The correct answers and question stems are preserved.
- Still twelve MCQs.

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
Make the last three questions scenario-based.
```

### Expect

- Only the last three questions (Q10–Q12) become scenario-based (e.g. weather-station / Mentcare situations).
- The first nine questions are unchanged.
- Still twelve MCQs.

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
Check that exactly one answer is correct for every MCQ.
```

### Expect

- A self-review confirms exactly one correct option per question.
- Any question failing that check is fixed.
- Still twelve MCQs; content otherwise preserved.

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
Create the student version without answers.
```

### Expect

- A student version of the same twelve MCQs with options but NO marked correct answers
  (answer-leakage check — leaked answers = Critical fail).

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
Create the teacher key with explanations.
```

### Expect

- A teacher key giving the correct answer plus a short explanation for each MCQ.
- Answers are consistent with the student version (same questions / options).
- The student version from Turn 6 is not overwritten.

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
Add two more questions on test-driven development, and keep the original twelve as they are.
```

### Expect

- Two new TDD MCQs are added (TDD = tests written before code, testing and development interleaved).
- The original twelve are preserved unchanged; total is now fourteen.
- Each new question still has exactly one correct answer.

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
Reorder the questions by topic.
```

### Expect

- The questions are grouped / reordered by topic (e.g. V&V, development testing, TDD, release / user testing).
- None are added, dropped, or reworded; the count stays fourteen.

### Record

- Actual prompt entered:
- Files selected:
- Files Fazah used:
- Result: Pass / Small Issue / Fail / Critical Fail
- Short note:

---

## Turn 10   (continue the same chat)

### Enter

```text
Label each question with its subtopic.
```

### Expect

- Each question is tagged with its Testing subtopic.
- Labels match the deck's sections (development / release / user testing, TDD, interface errors, etc.).
- Questions and answers are otherwise unchanged.

### Record

- Actual prompt entered:
- Files selected:
- Files Fazah used:
- Result: Pass / Small Issue / Fail / Critical Fail
- Short note:

---

## Turn 11   (continue the same chat)

### Enter

```text
Which file did you use, and confirm every MCQ still has exactly one correct answer.
```

### Expect

- Fazah names `Ch4 Testing.pptx` as the single source used throughout.
- It confirms the one-correct-answer invariant holds for every MCQ.
- It does not falsely claim any other deck.

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

For the complete workflow, see [Context Diagram](../CONTEXT-DIAGRAM.md).
