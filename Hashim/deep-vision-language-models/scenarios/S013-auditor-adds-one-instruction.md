# S013 — Auditor adds one instruction

## Tests

Fazah honors one auditor-added instruction on the opening turn and then carries the LLM/VLM/MLLM
definitions through a multi-turn workflow — examples, course exclusions, a check, a student
version, and source — without losing the base content or the added constraint.

## Setup

- Start: New chat
- Select files: `01_dvlm_introduction.pptx`
- Do not select: any other course file
- Turns: 6
- Auditor variation: Allowed — see the Auditor variation section

---

## Turn 1

### Enter

```text
explain the difference between llm, vlm and mllm for my class
```

(Then add exactly one instruction of your own — see the Auditor variation section.)

### Expect

- Definitions match the intro deck: **LLM** — trained primarily on language, understands and
  generates text; **VLM** — an LLM with a vision encoder, understands language + images, generates
  text; **MLLM** — a more general model built to process, understand, and generate multiple
  modalities (text, images, video, audio).
- Honors the one added instruction (format, length, audience, or example) while keeping the
  definitions correct.
- Grounded in `01_dvlm_introduction.pptx`, not a generic web answer.

### Record

- Actual prompt entered:
- Files selected:
- Files Fazah used:
- Result: Pass / Small Issue / Fail / Critical Fail
- Short note:

---

## Turn 2  (continue the same chat)

### Enter

```text
add one concrete example scenario for each of the 3
```

### Expect

- Gives one example scenario each for LLM, VLM, and MLLM that fits its definition correctly
  (e.g. a VLM example must involve image + language understanding with text output, not audio).
- The three definitions from turn 1 are preserved, not rewritten.
- Any instruction added in turn 1 (if a persistent one, e.g. audience) is still respected.

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
what does the course say it will NOT cover
```

### Expect

- Matches the intro deck's exclusion list: convolutions + attention, CNNs, RNNs, LSTMs,
  transformers, and how to train/evaluate/build/deploy AI models.
- Does not invent additional exclusions or claim excluded topics are covered.

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
make a 3 question check on the definitions
```

### Expect

- Produces exactly three questions covering the LLM/VLM/MLLM definitions.
- Questions draw only on the content covered above (e.g. "what does a VLM add to an LLM?" →
  a vision encoder), all answerable from the intro deck.

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
gimme a student version, no answers
```

### Expect

- Produces the three questions with NO answers shown.
- Answer leakage into the student version = Critical fail.
- Same three questions as turn 4, just without answers.

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
which file did this come from
```

### Expect

- Names the intro deck (`01_dvlm_introduction.pptx`) as the source.
- Does not claim any other or non-existent file.

### Record

- Actual prompt entered:
- Files selected:
- Files Fazah used:
- Result: Pass / Small Issue / Fail / Critical Fail
- Short note:

---

## Auditor variation

Add or change one realistic instruction on Turn 1. Record exactly what you entered. Do not change
the scenario's main goal or the later turns.

Example variations (append one to the Turn 1 prompt):

- "Use a table."
- "Keep it under 200 words."
- "Pitch it for students who have only done an intro ML course."
- "Add one everyday analogy."

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
