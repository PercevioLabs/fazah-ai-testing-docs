# S029 — Ten-question testing quiz refined into student + teacher versions

## Tests

Sustained multi-turn workflow on ONE testing quiz: Fazah creates exactly ten grounded questions, then
reorders, scenario-converts, de-duplicates, validates, and splits into student/teacher versions across
nine turns — each edit changing only what was asked while keeping the ten core questions intact.

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
Create exactly ten questions on software testing, with answers.
```

### Expect

- Exactly ten questions are created — not nine or eleven.
- Each question includes an answer (teacher-facing content is expected here).
- Questions are grounded in the Testing deck (e.g. verification vs. validation, testing stages/levels,
  interface errors, partition testing, TDD, alpha/beta/acceptance), not generic outside content.

### Record

- Actual prompt entered:
- Files selected:
- Files Fazah used:
- Result: Pass / Small Issue / Fail / Critical Fail
- Short note:

---

## Turn 2   (continue the same chat; keep `Ch4 Testing.pptx` selected)

### Enter

```text
Reorder them from easiest to hardest without changing the content.
```

### Expect

- The same ten questions appear, now ordered easiest → hardest.
- Question wording and answers are unchanged — only the order changes.
- The revision updates the existing quiz as a new version; nothing is added or removed.

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
Make the last three scenario-based.
```

### Expect

- The final three questions become scenario/applied items (e.g. a weather-station or Mentcare situation).
- The first seven questions are unchanged and still in easiest→hardest order.
- Still exactly ten questions; scenarios stay grounded in the Testing deck.

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
Replace any duplicate question.
```

### Expect

- Fazah checks for repeats and either replaces a duplicate or states none were found.
- Any replacement stays grounded in the Testing deck; the count stays at ten.
- All non-duplicate questions and the ordering/scenarios are preserved.

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
Check that each one has exactly one correct answer.
```

### Expect

- Fazah verifies each question has a single correct answer, fixing any with none/multiple.
- The check is auditable (per-question, or a clear statement all ten pass).
- No question content changes beyond what a correctness fix requires.

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
Now give me a student version with no answers.
```

### Expect

- A student version with the ten questions and answer space but NO answers (answer-leakage check).
- The questions match the current quiz (order, scenarios, ten items preserved).
- Answers leaking into the student version = Critical fail.

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
And a teacher key with explanations.
```

### Expect

- A teacher key gives each answer plus a short explanation grounded in the Testing deck.
- Answers/explanations align with the same ten questions.
- The student version from Turn 6 is not altered to include answers.

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
Add a three-question bonus section.
```

### Expect

- A separate bonus section of exactly three questions is added, grounded in the Testing deck.
- The ten core questions remain distinct from the bonus three.
- Bonus items are reflected consistently in the student version (no answers) and teacher key (answers).

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
Confirm the ten core questions are still there and tell me which file you used.
```

### Expect

- Fazah confirms the ten core questions (plus the three bonus) are intact.
- It names `Ch4 Testing.pptx` as the source and does not claim any deck it did not use.
- No new artifact is invented in the summary; it reflects what was actually produced.

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
