# S023 — Four essential attributes of good software

## Tests

With only the Introduction deck selected, Fazah sustains one workflow: it lists and explains the four
essential attributes of good software from Chapter 1, adds examples, reshapes them into a table and a
short quiz, produces a clean student version, and names its source — all without inventing extra
attributes or losing prior work.

## Setup

- Start: New chat
- Select files: `Ch1 Introduction.pptx`
- Do not select: any other deck
- Turns: 6
- Auditor variation: Not allowed

---

## Turn 1

### Enter

```text
What are the four essential attributes of good software? Give one short explanation of each.
```

### Expect

- The four attributes named match Chapter 1: **Maintainability**, **Dependability and security**,
  **Efficiency**, **Acceptability**.
- Each attribute gets one short, correct explanation (maintainability = can evolve to meet changing
  needs; efficiency = does not waste system resources; acceptability = usable/understandable by
  intended users).
- No extra invented attributes beyond the four; reply grounded in the selected Introduction deck.

### Record

- Actual prompt entered:
- Files selected:
- Files Fazah used:
- Result: Pass / Small Issue / Fail / Critical Fail
- Short note:

---

## Turn 2   (continue the same chat; keep `Ch1 Introduction.pptx` selected)

### Enter

```text
Now give a one-line example of each.
```

### Expect

- One short example per attribute, each mapped to the correct attribute from Turn 1 (e.g. evolving a
  tool for a new rule → maintainability; no data loss on failure → dependability and security).
- Still exactly four attributes; no fifth attribute or off-topic example is introduced.
- Examples stay consistent with the Introduction deck rather than generic software claims.

### Record

- Actual prompt entered:
- Files selected:
- Files Fazah used:
- Result: Pass / Small Issue / Fail / Critical Fail
- Short note:

---

## Turn 3   (continue the same chat; keep `Ch1 Introduction.pptx` selected)

### Enter

```text
Turn it into a table.
```

### Expect

- A table with the four attributes as rows, columns for explanation and example carried from Turns 1–2.
- Content matches the earlier turns (same four attributes, same explanations); nothing is dropped or
  silently reworded into a wrong meaning.
- No fifth row or invented attribute appears.

### Record

- Actual prompt entered:
- Files selected:
- Files Fazah used:
- Result: Pass / Small Issue / Fail / Critical Fail
- Short note:

---

## Turn 4   (continue the same chat; keep `Ch1 Introduction.pptx` selected)

### Enter

```text
Make four questions from this, one per attribute.
```

### Expect

- Exactly four questions, one targeting each of the four attributes.
- Questions are answerable from the table/explanations already built, not on uncovered Chapter 1 depth.
- Content stays grounded in the Introduction deck; no new attributes smuggled in.

### Record

- Actual prompt entered:
- Files selected:
- Files Fazah used:
- Result: Pass / Small Issue / Fail / Critical Fail
- Short note:

---

## Turn 5   (continue the same chat; keep `Ch1 Introduction.pptx` selected)

### Enter

```text
Give me a student version of those four questions with no answers.
```

### Expect

- The same four questions from Turn 4, with all answers/explanations removed.
- No answer or attribute definition leaks into the student version (answers leaking = Critical fail).
- Question set is unchanged in count and topic (still one per attribute).

### Record

- Actual prompt entered:
- Files selected:
- Files Fazah used:
- Result: Pass / Small Issue / Fail / Critical Fail
- Short note:

---

## Turn 6   (continue the same chat; keep `Ch1 Introduction.pptx` selected)

### Enter

```text
Which file did all of this come from?
```

### Expect

- Fazah names `Ch1 Introduction.pptx` (the Introduction deck) as the source.
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
