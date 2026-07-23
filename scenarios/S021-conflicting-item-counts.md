# S021 — Conflicting item counts

## Tests

Fazah detects a contradiction inside a single prompt (asking for 10 questions and exactly 15 at
once) instead of silently resolving it, then carries the resolved count consistently through a
sustained build workflow (produce, answers, student version, count check).

## Setup

- Start: New chat
- Select files: none (Turns 1–2); then select `Ch4 Testing.pptx` before Turn 3 (kept selected after)
- Do not select: any deck during the contradiction turns (1–2)
- Turns: 6
- Auditor variation: Not allowed

---

## Turn 1

### Enter

```text
Create 10 questions and keep the assessment to exactly 15 questions.
```

### Expect

- Detects the contradiction between "10 questions" and "exactly 15 questions".
- Either asks which count is intended OR states an assumed count while explicitly flagging the
  conflict — at most one short clarification.
- Does NOT silently pick one number and present the result as if the request were consistent.

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
Let's make it 12.
```

### Expect

- Accepts 12 as the resolved count and drops the earlier conflicting 10 / 15.
- Does not re-raise the contradiction or re-ask the count.

### Record

- Actual prompt entered:
- Files selected:
- Files Fazah used:
- Result: Pass / Small Issue / Fail / Critical Fail
- Short note:

---

## Turn 3   (SELECT `Ch4 Testing.pptx` in Course Files before entering)

### Enter

```text
Go ahead and produce the 12 questions from this file.
```

### Expect

- Exactly twelve questions — matching the resolved count, not 10 or 15.
- Grounded in the selected Testing deck (`Ch4 Testing.pptx`); no fabricated content.
- Shows the Testing file as the used source.

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
Add answers to all of them.
```

### Expect

- Adds a correct answer to each of the same twelve questions; questions unchanged.
- Still exactly twelve; answers grounded in the Testing deck.

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
Give me a student version with no answers.
```

### Expect

- Produces a student version of the same twelve questions with answer space but NO answers.
- No correct answers leak into the student version (leakage = Critical fail).
- Still exactly twelve questions.

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
Confirm the count is 12.
```

### Expect

- Confirms the assessment has exactly twelve questions, consistent with Turns 2–5.
- Reports the actual count honestly (not 10 or 15); no silent mismatch.

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
