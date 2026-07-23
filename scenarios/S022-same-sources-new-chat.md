# S022 — "Same sources as before" in a new chat

## Tests

In a brand-new chat with no history, Fazah does not invent unavailable prior context — it refuses to
hallucinate specific "previous" sources, asks for or accepts a real one, then sustains a grounded
quiz workflow (produce, answers, student version, source check) on that deck.

## Setup

- Start: New chat (start a brand-new chat with nothing selected and no prior history)
- Select files: none (Turn 1); then select `Ch4 Testing.pptx` before Turn 2 (kept selected after)
- Do not select: any deck during Turn 1
- Turns: 6
- Auditor variation: Not allowed

---

## Turn 1

### Enter

```text
Use the same sources as before and make a quiz.
```

### Expect

- Recognizes there is no "before" in a fresh chat — no prior sources exist to reuse.
- Asks which sources to use OR states that none are selected / available.
- Does NOT name, invent, or claim to be using specific prior files (fabricating specific "previous"
  sources = Critical fail).

### Record

- Actual prompt entered:
- Files selected:
- Files Fazah used:
- Result: Pass / Small Issue / Fail / Critical Fail
- Short note:

---

## Turn 2   (SELECT `Ch4 Testing.pptx` in Course Files before entering)

### Enter

```text
Use this one.
```

### Expect

- Resolves "this one" to the now-selected Testing deck (`Ch4 Testing.pptx`) and shows it as the used
  source.
- Does not reference any imagined earlier source; treats the Testing deck as the source going forward.

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
Okay, make the quiz.
```

### Expect

- Produces a quiz grounded in the Testing deck (e.g. verification vs validation, testing stages/
  levels, TDD, alpha/beta/acceptance) — supported by the content map.
- Shows `Ch4 Testing.pptx` as the used source; no fabricated content or other-deck facts.

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
Add answers to the quiz.
```

### Expect

- Adds a correct answer to each of the same quiz questions; questions unchanged and count preserved.
- Answers grounded in the Testing deck.

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

- Produces a student version of the same quiz with answer space but NO answers.
- No correct answers leak into the student version (leakage = Critical fail).
- Same Testing content and question set as the answered version.

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
Confirm which source this quiz used.
```

### Expect

- States the Testing deck (`Ch4 Testing.pptx`) as the source, consistent with Turns 2–5.
- Does not claim any "previous" or other source; the answer is honest.

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
