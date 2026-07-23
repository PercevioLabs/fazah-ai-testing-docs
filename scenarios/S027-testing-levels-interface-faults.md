# S027 — Testing levels and interface faults

## Tests

With only the Testing deck selected, Fazah sustains one workflow: it explains the three levels of
development testing with correct interface-error examples, adds partition (equivalence) testing,
builds a five-question set including scenario items, adds answers, produces a clean student version,
and confirms its source — retaining context across turns.

## Setup

- Start: New chat
- Select files: `Ch4 Testing.pptx`
- Do not select: any other deck
- Turns: 7
- Auditor variation: Not allowed

---

## Turn 1

### Enter

```text
Explain unit, component, and system testing, and give a short example of interface misuse, interface misunderstanding, and a timing error.
```

### Expect

- Unit testing = individual functions/methods/object classes in isolation; component testing =
  composite components, focus on component interfaces; system testing = the integrated system, focus
  on component interactions / emergent behaviour.
- Interface misuse = a calling component uses the interface wrongly (e.g. parameters in wrong order);
  interface misunderstanding = the caller makes incorrect assumptions about the called component.
- Timing error = caller and called component run at different speeds and out-of-date information is
  used; grounded in the selected Testing deck.

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
Add partition (equivalence) testing to this.
```

### Expect

- Describes partition/equivalence testing per Chapter 8: group inputs into partitions expected to
  behave similarly, then test from each partition (including boundaries).
- Presented as a testing strategy alongside the levels/interface material, not replacing it.
- Content stays grounded in the Testing deck.

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
Make five questions across these topics.
```

### Expect

- Exactly five questions spanning the testing levels, the three interface errors, and partition
  testing built above.
- Questions are answerable from the deck material, not on uncovered testing depth.
- Content stays grounded in the Testing deck.

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
Make two of them scenario-based.
```

### Expect

- Two of the five questions become short scenario/applied items (e.g. spot the interface error in a
  described situation), the other three preserved.
- Still exactly five questions total; count and topic coverage retained from Turn 3.
- Scenarios stay within deck-covered concepts (interface errors, levels, partitions).

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
Add answers.
```

### Expect

- A correct answer/key for each of the five questions, including the two scenario items.
- Answers are correct against the deck (right level, right interface-error type, right partition
  reasoning).
- The key matches the same five questions; no new questions invented.

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
Now give me a student version with no answers.
```

### Expect

- The same five questions (including the two scenarios), with all answers/keys removed.
- No answer leaks into the student version (answers leaking = Critical fail).
- Question count and topics are unchanged from Turns 3–5.

### Record

- Actual prompt entered:
- Files selected:
- Files Fazah used:
- Result: Pass / Small Issue / Fail / Critical Fail
- Short note:

---

## Turn 7   (continue the same chat; keep `Ch4 Testing.pptx` selected)

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
