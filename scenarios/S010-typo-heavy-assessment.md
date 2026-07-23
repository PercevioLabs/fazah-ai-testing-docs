# S010 — Typo-heavy assessment request

## Tests

Fazah parses typo-heavy prompts correctly across a full assessment workflow — build, edit, reorder,
student/teacher split, add items, consistency check, source — without dropping the item count or
misreading the misspelled instructions.

## Setup

- Start: New chat
- Select files: `Ch4 Testing.pptx`
- Do not select: any other deck
- Turns: 8
- Auditor variation: Not allowed

---

## Turn 1

### Enter

```text
make 10 mcq frm testng hard with answrs n short explaination
```

### Expect

- Reads the typos correctly: topic = testing, multiple-choice questions.
- Exactly 10 MCQs at a hard difficulty level, each with the correct answer and a short explanation.
- Content is grounded in the selected Testing deck (`Ch4 Testing.pptx`), not generic web material.

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
q4 too ez make it hardr
```

### Expect

- Only question 4 is made harder; the other nine questions are unchanged.
- Still exactly 10 MCQs (a new version of the same quiz).
- Q4 keeps one correct answer and its explanation.

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
reordr esiest to hardst
```

### Expect

- Same 10 questions reordered from easiest to hardest — no questions added or removed.
- Answers and explanations stay attached to their questions after reordering.

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
make studnt version no answrs
```

### Expect

- Produces a student version of the same 10 questions with NO answers or explanations shown.
- Answer leakage into the student version = Critical fail.
- Question order from turn 3 is preserved.

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
teachr key w explanations
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

## Turn 6   (continue the same chat)

### Enter

```text
add 2 scenario qs at the end keep 10 total
```

### Expect

- Reads the intent: add two scenario-based questions at the end but the total must stay 10.
- Ends with exactly 10 questions — the last two are scenario-based (e.g. weather station / Mentcare).
- Earlier questions are trimmed/replaced to keep the total at 10, not simply appended to make 12.

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
chek only 1 ans is corect each
```

### Expect

- Confirms each of the 10 questions has exactly one correct answer.
- Flags and fixes any question with zero or multiple correct options (if any).

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
wich file did u use
```

### Expect

- Names the Testing deck (`Ch4 Testing.pptx`) as the source.
- Does not claim any other or non-existent file.

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
