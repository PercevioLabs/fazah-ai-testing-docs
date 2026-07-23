# S024 — Waterfall vs incremental development

## Tests

With only the Processes deck selected, Fazah sustains one comparison workflow: it contrasts waterfall
and incremental development accurately, fits each to a realistic situation, adds limitations, reshapes
into a table and a quiz, produces a student version, and confirms its source — staying within how the
lecture frames them across all turns.

## Setup

- Start: New chat
- Select files: `Ch2 SW Processes.pptx`
- Do not select: any other deck
- Turns: 7
- Auditor variation: Allowed — see the Auditor variation section

---

## Turn 1

### Enter

```text
Compare waterfall and incremental development.
```

### Expect

- Waterfall described per Chapter 2: **plan-driven**, separate/sequential phases, main drawback =
  hard to accommodate change once underway.
- Incremental described per Chapter 2: specification/development/validation **interleaved**, reduced
  cost of change, easier customer feedback and faster delivery.
- Grounded in the selected Processes deck (badge / Processes under used sources).

### Record

- Actual prompt entered:
- Files selected:
- Files Fazah used:
- Result: Pass / Small Issue / Fail / Critical Fail
- Short note:

---

## Turn 2   (continue the same chat; keep `Ch2 SW Processes.pptx` selected)

### Enter

```text
Give me one realistic project situation where each approach fits, staying within how the lecture frames them.
```

### Expect

- Waterfall situation matches the lecture: stable, well-understood requirements / large
  systems-engineering projects.
- Incremental situation matches the lecture: changing requirements / need for early delivery and
  customer feedback.
- Both build on the Turn 1 comparison and neither contradicts the slides.

### Record

- Actual prompt entered:
- Files selected:
- Files Fazah used:
- Result: Pass / Small Issue / Fail / Critical Fail
- Short note:

---

## Turn 3   (continue the same chat; keep `Ch2 SW Processes.pptx` selected)

### Enter

```text
Add one limitation of each.
```

### Expect

- Waterfall limitation matches Chapter 2 (e.g. change is hard/expensive once phases are underway).
- Incremental limitation matches Chapter 2 (e.g. reduced process visibility; structure degrades
  without refactoring).
- Limitations attach to the correct approach and extend, not overwrite, the Turn 1–2 material.

### Record

- Actual prompt entered:
- Files selected:
- Files Fazah used:
- Result: Pass / Small Issue / Fail / Critical Fail
- Short note:

---

## Turn 4   (continue the same chat; keep `Ch2 SW Processes.pptx` selected)

### Enter

```text
Put it in a table.
```

### Expect

- A table comparing waterfall and incremental with rows/columns covering description, fitting
  situation, and limitation carried from Turns 1–3.
- Content stays consistent with the earlier turns; nothing is dropped or reassigned to the wrong
  approach.
- No fabricated process model or extra column of invented facts is added.

### Record

- Actual prompt entered:
- Files selected:
- Files Fazah used:
- Result: Pass / Small Issue / Fail / Critical Fail
- Short note:

---

## Turn 5   (continue the same chat; keep `Ch2 SW Processes.pptx` selected)

### Enter

```text
Make four questions from this comparison.
```

### Expect

- Exactly four questions covering the waterfall/incremental contrast built above.
- Questions are answerable from the deck material (phases, change accommodation, visibility,
  fitting situations), not on uncovered agile/XP detail.
- Content stays grounded in the Processes deck.

### Record

- Actual prompt entered:
- Files selected:
- Files Fazah used:
- Result: Pass / Small Issue / Fail / Critical Fail
- Short note:

---

## Turn 6   (continue the same chat; keep `Ch2 SW Processes.pptx` selected)

### Enter

```text
Give me a student version with no answers.
```

### Expect

- The same four questions from Turn 5, with all answers/explanations removed.
- No answer or comparison key leaks into the student version (answers leaking = Critical fail).
- Question count and topics are unchanged.

### Record

- Actual prompt entered:
- Files selected:
- Files Fazah used:
- Result: Pass / Small Issue / Fail / Critical Fail
- Short note:

---

## Turn 7   (continue the same chat; keep `Ch2 SW Processes.pptx` selected)

### Enter

```text
Which file did you use for all of this?
```

### Expect

- Fazah names `Ch2 SW Processes.pptx` (the Processes deck) as the source.
- No other deck is claimed as a source for this comparison.
- Answer is consistent with the used-sources shown across the conversation.

### Record

- Actual prompt entered:
- Files selected:
- Files Fazah used:
- Result: Pass / Small Issue / Fail / Critical Fail
- Short note:

---

## Auditor variation

Add or change one realistic instruction. Record exactly what you entered. Do not change the
scenario's main goal (the sustained waterfall-vs-incremental workflow).

Examples:
- "Put the comparison in a table." (bring the table request earlier)
- "Add a limitation of each approach."
- "Make it suitable for first-year students."
- "Keep it under 200 words."

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
