# S018 — Clear topic, indirect source name

## Tests

Fazah maps an indirect source description ("the chapter about testing") to the correct file, then
sustains a grounded multi-turn workflow (explain, exemplify, generate, verify source, produce a
student version) all anchored to that one deck.

## Setup

- Start: New chat
- Select files: none
- Do not select: any deck (Fazah must resolve the source from the wording, not a selection)
- Turns: 6
- Auditor variation: Not allowed

---

## Turn 1

### Enter

```text
use the chapter about testing n explain the three stages of development testing
```

### Expect

- Maps "the chapter about testing" to the Testing deck (`Ch4 Testing.pptx`) and shows it as the used
  source; does not invent or cite a source it cannot map.
- Names the three levels of development testing: unit testing (individual functions / methods /
  objects), component testing (component interfaces), system testing (component interactions /
  emergent behaviour).
- Grounded in the Testing deck; no fabricated content or facts attributed to other decks.

### Record

- Actual prompt entered:
- Files selected:
- Files Fazah used:
- Result: Pass / Small Issue / Fail / Critical Fail
- Short note:

---

## Turn 2   (continue the same chat)

### Enter

```text
gimme a short example for each of those 3 levels
```

### Expect

- One short example per level, tied to the same unit/component/system breakdown from Turn 1.
- Examples stay consistent with the Testing deck (e.g. weather-station object tests, component
  interfaces, emergent behaviour); no fabricated outside cases attributed to the slides.
- Does not switch topics or decks.

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
now make 3 questions on this
```

### Expect

- Exactly three questions about development testing / the three levels just discussed.
- Grounded in the Testing deck; no Requirements or Agile content pulled in.
- Builds on the accumulated topic rather than restarting.

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
which file did u map that to
```

### Expect

- States the Testing deck (`Ch4 Testing.pptx`) as the source it resolved and used.
- Honest and consistent with Turns 1–3; does not name a deck it did not use.

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
add answers to the 3 questions
```

### Expect

- Adds a correct answer to each of the same three questions; questions themselves unchanged.
- Answers grounded in the Testing deck; still exactly three questions.

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
gimme a student version without the answers
```

### Expect

- Produces a student version of the same three questions with answer space but NO answers shown.
- No correct answers leak into the student version (leakage = Critical fail).
- Same Testing content and question set as the answered version.

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
