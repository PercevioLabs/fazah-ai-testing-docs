# S007 — Current explicit selection overrides recent source history

## Tests

When the current explicit file selection conflicts with the recent conversation source, Fazah honors
the newly-selected Testing file rather than the earlier Agile context, and then holds that source
through a sustained workflow — more Testing concepts, questions, a source check, a reorder, and a
student version.

## Setup

- Start: New chat
- Select files: `Ch5 Agile SW Dev.pptx` first (Turn 1), then deselect it and select
  `Ch4 Testing.pptx` (Turn 2 onward)
- Do not select: any other deck
- Turns: 7
- Auditor variation: Not allowed

---

## Turn 1  (select `Ch5 Agile SW Dev.pptx`)

### Enter

```text
Explain Scrum.
```

### Expect

- Grounded in the Agile deck (`Ch5 Agile SW Dev.pptx`).
- Scrum roles/terms correct: sprints (2–4 weeks), product backlog, product owner, ScrumMaster,
  daily Scrum.
- Used sources reflect the Agile deck.

### Record

- Actual prompt entered:
- Files selected:
- Files Fazah used:
- Result: Pass / Small Issue / Fail / Critical Fail
- Short note:

---

## Turn 2  (before entering: deselect Agile, select `Ch4 Testing.pptx`; continue the same chat)

### Enter

```text
Explain test-driven development.
```

### Expect

- Fazah uses the now-explicitly-selected Testing deck (grounding badge / used sources reflect
  Testing), overriding the recent Agile context.
- TDD explained correctly: tests written before the code, interleaved and incremental, driven by
  automated tests.
- The answer is not attributed to the Agile deck from Turn 1.

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
Keep using the Testing file — explain unit versus component testing.
```

### Expect

- Unit testing = testing the functionality of individual objects/methods; component testing = testing
  component interfaces / interactions between units.
- Still grounded in `Ch4 Testing.pptx`; no return to the Agile deck.

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
Make five questions from the Testing file.
```

### Expect

- Exactly five questions, covering the Testing material discussed (TDD, unit/component testing, etc.).
- Grounded in the Testing deck; each question is answerable from it.

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
Which file are these questions from?
```

### Expect

- Fazah names the Testing deck (`Ch4 Testing.pptx`).
- It does not credit the Agile deck from Turn 1.

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
Reorder them from easy to hard.
```

### Expect

- The same five questions, reordered easy → hard; none added, dropped, or rewritten in substance.
- Still grounded in the Testing deck.

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
Give me a student version.
```

### Expect

- The same five questions (in the easy→hard order) as a student-facing version with NO answers shown
  (answer-leakage check — leaked answers = Critical fail).
- Order and content from Turn 6 are preserved.

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
