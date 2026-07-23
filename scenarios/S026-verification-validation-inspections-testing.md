# S026 — Verification, validation, inspections, and testing

## Tests

With only the Testing deck selected, Fazah sustains one workflow: it gives a structured explanation
that separates verification, validation, inspections, and testing, then adds examples, a table, a
quiz, a clean student version, and confirms its source — keeping all four concepts distinct across
turns.

## Setup

- Start: New chat
- Select files: `Ch4 Testing.pptx`
- Do not select: any other deck
- Turns: 6
- Auditor variation: Not allowed

---

## Turn 1

### Enter

```text
Give a concise structured explanation that distinguishes verification, validation, inspections, and testing.
```

### Expect

- Verification = "are we building the product **right**?" (conform to specification); validation =
  "are we building the **right** product?" (meet the user's real needs).
- Inspections = **static** verification (examine the static representation, no execution required,
  usable before implementation); testing = **dynamic** verification (execute with test data and
  observe behaviour).
- All four are clearly distinguished, grounded in the selected Testing deck.

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
Give an example of each.
```

### Expect

- One example per concept, correctly matched (e.g. checking code against the spec → verification;
  checking the system meets user needs → validation; a code/design review with no execution →
  inspection; running test data → testing).
- Examples keep static (inspection) vs dynamic (testing) and right-vs-right-product distinctions
  correct.
- Still exactly the four concepts; examples stay grounded in the Testing deck.

### Record

- Actual prompt entered:
- Files selected:
- Files Fazah used:
- Result: Pass / Small Issue / Fail / Critical Fail
- Short note:

---

## Turn 3   (continue the same chat; keep `Ch4 Testing.pptx` selected)

### Enter

```text
Put it in a table.
```

### Expect

- A table with the four concepts as rows and columns for definition and example carried from Turns 1–2.
- Content matches the earlier turns; verification/validation and inspections/testing are not swapped
  or merged.
- No fifth concept or invented fact is added.

### Record

- Actual prompt entered:
- Files selected:
- Files Fazah used:
- Result: Pass / Small Issue / Fail / Critical Fail
- Short note:

---

## Turn 4   (continue the same chat; keep `Ch4 Testing.pptx` selected)

### Enter

```text
Make four questions from this, one per concept.
```

### Expect

- Exactly four questions, one targeting each of verification, validation, inspections, testing.
- Questions are answerable from the table/explanations already built, not on uncovered testing depth.
- Content stays grounded in the Testing deck.

### Record

- Actual prompt entered:
- Files selected:
- Files Fazah used:
- Result: Pass / Small Issue / Fail / Critical Fail
- Short note:

---

## Turn 5   (continue the same chat; keep `Ch4 Testing.pptx` selected)

### Enter

```text
Give me a student version with no answers.
```

### Expect

- The same four questions from Turn 4, with all answers/explanations removed.
- No answer or definition key leaks into the student version (answers leaking = Critical fail).
- Question count and topics are unchanged (still one per concept).

### Record

- Actual prompt entered:
- Files selected:
- Files Fazah used:
- Result: Pass / Small Issue / Fail / Critical Fail
- Short note:

---

## Turn 6   (continue the same chat; keep `Ch4 Testing.pptx` selected)

### Enter

```text
Confirm which file all of this came from.
```

### Expect

- Fazah names `Ch4 Testing.pptx` (the Testing deck) as the source.
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

For the complete workflow, see [Context Diagram](../CONTEXT-DIAGRAM.md).
