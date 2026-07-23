# S019 — "Use these slides" with no source

## Tests

Fazah recovers a deictic reference ("these slides") that has no referent when no file is selected,
resolves it once a file is selected, then sustains a grounded build-questions workflow (answers,
selective edit, reorder, student version, source check) on that resolved deck.

## Setup

- Start: New chat
- Select files: none (Turn 1); then select `Ch3 Req Eng.pptx` before Turn 2 (kept selected after)
- Do not select: any deck during Turn 1
- Turns: 7
- Auditor variation: Not allowed

---

## Turn 1

### Enter

```text
Use these slides and make five questions.
```

### Expect

- Because no file is selected, "these slides" has no referent — Fazah asks which slides / files to
  use (at most one short clarifying question).
- Does NOT invent a source, silently pick a deck, or fabricate slide content to answer.

### Record

- Actual prompt entered:
- Files selected:
- Files Fazah used:
- Result: Pass / Small Issue / Fail / Critical Fail
- Short note:

---

## Turn 2   (SELECT `Ch3 Req Eng.pptx` in Course Files before entering)

### Enter

```text
These ones.
```

### Expect

- Resolves "these ones" to the now-selected Requirements deck (`Ch3 Req Eng.pptx`) and shows it as
  the used source.
- Exactly five questions, grounded in the Requirements deck (e.g. functional vs non-functional,
  elicitation, validation checks) — supported by the content map; no fabricated content.

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
Add answers to each one.
```

### Expect

- Adds a correct answer to each of the same five questions; questions unchanged.
- Answers grounded in the Requirements deck; still exactly five questions.

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
Turn question 2 into a scenario question.
```

### Expect

- Only question 2 becomes a scenario-based question (e.g. a Mentcare / iLearn / insulin-pump
  situation from the deck); the other four are preserved.
- Still five questions, still Requirements-grounded; the scenario is not fabricated outside the deck.
- Updates the active artifact as a new version.

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
Reorder them from foundational to advanced.
```

### Expect

- The same five questions are reordered easiest/foundational first, hardest/most advanced last.
- No question is dropped, added, or rewritten by the reorder — only sequence changes; the scenario
  question from Turn 4 is retained.

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
Give me a student version with no answers.
```

### Expect

- Produces a student version of the same five (reordered) questions with answer space but NO answers.
- No correct answers leak into the student version (leakage = Critical fail).
- Same Requirements content, question set, and order as the answered version.

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
Confirm which source these came from.
```

### Expect

- States the Requirements deck (`Ch3 Req Eng.pptx`) as the source, consistent with Turns 2–6.
- Does not claim any other deck; the answer is honest.

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
