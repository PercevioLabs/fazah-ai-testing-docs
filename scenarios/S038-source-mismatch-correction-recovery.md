# S038 — Recovering gracefully from a wrong-source start

## Tests

Across ten turns Fazah honestly flags that the selected Agile deck can't answer a requirements question,
recovers after the correct Requirements file is selected, builds FR/NFR artifacts from it, and repeatedly
reports the true source without ever claiming the Agile deck.

## Setup

- Start: New chat
- Select files: `Ch5 Agile SW Dev.pptx` (intentionally the wrong deck for this task)
- Do not select: `Ch3 Req Eng.pptx` yet — it is selected mid-scenario at Turn 3
- Turns: 10
- Auditor variation: Not allowed

---

## Turn 1   (`Ch5 Agile SW Dev.pptx` selected)

### Enter

```text
Explain functional and non-functional requirements using the selected file.
```

### Expect

- Fazah notes honestly that the selected Agile deck does not cover functional / non-functional
  requirements, and asks for or offers the right file (Requirements).
- It does NOT fabricate requirements content attributed to the Agile deck (fabrication = Critical fail).

### Record

- Actual prompt entered:
- Files selected:
- Files Fazah used:
- Result: Pass / Small Issue / Fail / Critical Fail
- Short note:

---

## Turn 2   (continue the same chat; Agile still selected)

### Enter

```text
You're right — that was the wrong deck.
```

### Expect

- Fazah acknowledges the correction.
- It offers to use the correct Requirements material.
- It does not proceed to invent an answer from the Agile deck.

### Record

- Actual prompt entered:
- Files selected:
- Files Fazah used:
- Result: Pass / Small Issue / Fail / Critical Fail
- Short note:

---

## Turn 3   (continue the same chat; NOW select `Ch3 Req Eng.pptx`)

### Enter

```text
Use this Requirements file now.
```

### Expect

- Fazah switches to the Requirements deck as the working source.
- It confirms it will now draw on `Ch3 Req Eng.pptx`.

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
Now explain functional versus non-functional requirements using the corrected source.
```

### Expect

- Functional requirements = statements of services the system should provide / how it behaves;
  non-functional = constraints on services / functions (timing, standards), often whole-system.
- Grounded in `Ch3 Req Eng.pptx`, not the Agile deck.

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
Put it in a comparison table.
```

### Expect

- An FR vs NFR comparison table.
- Content matches the Turn 4 explanation; no new unsupported claims.
- Grounded in the Requirements deck.

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
Make five student questions from that table.
```

### Expect

- Exactly five student-facing questions derived from the FR vs NFR table.
- Grounded in the Requirements deck.

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
Which source did you use for that last artifact?
```

### Expect

- Fazah correctly states it used the Requirements deck (`Ch3 Req Eng.pptx`).
- It does NOT claim the Agile deck.
- It does not falsely claim a source it did not use (false claim = Critical fail).

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
Add a teacher key for those five questions.
```

### Expect

- A teacher key with answers for the same five questions.
- Answers are grounded in the Requirements deck and consistent with the table.
- The five questions themselves are unchanged.

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
Now give me a student version with no answers.
```

### Expect

- A student version of the five questions with NO answers shown (answer-leakage check —
  leaked answers = Critical fail).
- The teacher key from Turn 8 is not overwritten.

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
Confirm the corrected source fed every artifact in this chat.
```

### Expect

- Fazah confirms the FR/NFR explanation, table, questions, teacher key, and student version all came
  from `Ch3 Req Eng.pptx`.
- It notes the Agile deck was not used after the correction.
- No fabricated source and no false claim of the Agile deck.

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
