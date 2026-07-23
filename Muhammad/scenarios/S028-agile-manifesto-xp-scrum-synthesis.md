# S028 — Agile Manifesto, XP, and Scrum synthesis

## Tests

Multi-step synthesis inside one source (the Agile deck): Fazah builds from the Manifesto values to XP
support, an XP↔Scrum comparison and table, student quick-check questions with a teacher key and a
clean student version, a Scrum-roles question, and a final source confirmation — retaining context
across all turns.

## Setup

- Start: New chat
- Select files: `Ch5 Agile SW Dev.pptx`
- Do not select: any other deck
- Turns: 9
- Auditor variation: Not allowed

---

## Turn 1

### Enter

```text
what are the 4 values of the agile manifesto
```

### Expect

- Lists the four values per Chapter 3/Agile deck: individuals and interactions over processes and
  tools; working software over comprehensive documentation; customer collaboration over contract
  negotiation; responding to change over following a plan.
- Grounded in the selected Agile deck (badge / Agile under used sources).

### Record

- Actual prompt entered:
- Files selected:
- Files Fazah used:
- Result: Pass / Small Issue / Fail / Critical Fail
- Short note:

---

## Turn 2   (continue the same chat; keep `Ch5 Agile SW Dev.pptx` selected)

### Enter

```text
ok how do XP practices support those values
```

### Expect

- Maps XP practices to the four values (e.g. small/frequent releases → responding to change; on-site
  customer → customer collaboration; pair programming / collective ownership → individuals and
  interactions; test-first development / refactoring → working software).
- Practices named are real XP practices from the deck and reference the Turn 1 values.

### Record

- Actual prompt entered:
- Files selected:
- Files Fazah used:
- Result: Pass / Small Issue / Fail / Critical Fail
- Short note:

---

## Turn 3   (continue the same chat; keep `Ch5 Agile SW Dev.pptx` selected)

### Enter

```text
and how does scrum differ from XP
```

### Expect

- Scrum framed as a **management** framework for iterative development (sprints, product backlog,
  roles); XP framed as **technical** practices.
- Distinction is consistent with the prior turns and grounded in the Agile deck.

### Record

- Actual prompt entered:
- Files selected:
- Files Fazah used:
- Result: Pass / Small Issue / Fail / Critical Fail
- Short note:

---

## Turn 4   (continue the same chat; keep `Ch5 Agile SW Dev.pptx` selected)

### Enter

```text
put XP vs scrum in a compact comparison table
```

### Expect

- A compact table comparing XP and Scrum, consistent with Turns 2–3 (XP = technical practices;
  Scrum = management framework).
- No fabricated facts beyond what the deck supports.

### Record

- Actual prompt entered:
- Files selected:
- Files Fazah used:
- Result: Pass / Small Issue / Fail / Critical Fail
- Short note:

---

## Turn 5   (continue the same chat; keep `Ch5 Agile SW Dev.pptx` selected)

### Enter

```text
now turn that table into 3 quick-check questions for students
```

### Expect

- Exactly three student quick-check questions derived from the Turn 4 table.
- Synthesis from earlier turns retained (Manifesto values / XP / Scrum, not off-topic material).
- Questions are student-facing; any answers are clearly marked, not mixed into the prompts.

### Record

- Actual prompt entered:
- Files selected:
- Files Fazah used:
- Result: Pass / Small Issue / Fail / Critical Fail
- Short note:

---

## Turn 6   (continue the same chat; keep `Ch5 Agile SW Dev.pptx` selected)

### Enter

```text
add a teacher key for those
```

### Expect

- A teacher key with correct answers for the three questions from Turn 5.
- Answers correct against the deck (right XP/Scrum distinction, right Manifesto values).
- The key matches the same three questions; no new questions invented.

### Record

- Actual prompt entered:
- Files selected:
- Files Fazah used:
- Result: Pass / Small Issue / Fail / Critical Fail
- Short note:

---

## Turn 7   (continue the same chat; keep `Ch5 Agile SW Dev.pptx` selected)

### Enter

```text
ok now a student version, no answers
```

### Expect

- The same three questions from Turn 5, with all answers/keys removed.
- No answer leaks into the student version (answers leaking = Critical fail).
- Question count and topics are unchanged.

### Record

- Actual prompt entered:
- Files selected:
- Files Fazah used:
- Result: Pass / Small Issue / Fail / Critical Fail
- Short note:

---

## Turn 8   (continue the same chat; keep `Ch5 Agile SW Dev.pptx` selected)

### Enter

```text
add one question on scrum roles — product owner, ScrumMaster and the development team
```

### Expect

- One added question on Scrum roles, naming product owner, ScrumMaster, and development team per the
  deck.
- Roles are described correctly (e.g. product owner owns the backlog; ScrumMaster facilitates;
  development team ≤7 builds the increment).
- Added to the existing set (student version stays answer-free if extended).

### Record

- Actual prompt entered:
- Files selected:
- Files Fazah used:
- Result: Pass / Small Issue / Fail / Critical Fail
- Short note:

---

## Turn 9   (continue the same chat; keep `Ch5 Agile SW Dev.pptx` selected)

### Enter

```text
confirm all this came from the agile deck
```

### Expect

- Fazah confirms `Ch5 Agile SW Dev.pptx` (the Agile deck) as the source for all of it.
- No other deck is claimed as a source for this material.
- Answer is consistent with the used-sources shown across the conversation.

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
