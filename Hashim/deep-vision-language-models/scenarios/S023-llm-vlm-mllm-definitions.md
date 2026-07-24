# S023 — LLM vs VLM vs MLLM definitions

## Tests

With only the introduction deck selected, Fazah sustains one workflow: it gives the deck's exact
LLM / VLM / MLLM definitions, holds the line on what a VLM can generate, reshapes the
definitions into a table and a matching exercise with a key, and names its source — all without
inventing capabilities the deck never claims.

## Setup

- Start: New chat
- Select files: `01_dvlm_introduction.pptx`
- Do not select: any other file
- Turns: 6
- Auditor variation: Not allowed

---

## Turn 1

### Enter

```text
whats the difference between an LLM, a VLM and an MLLM? short definitions pls
```

### Expect

- Definitions match the intro deck: **LLM** = large model primarily trained on language, able to
  understand and generate text; **VLM** = an LLM with a vision encoder, allowing it to understand
  language and images and generate text; **MLLM** = a more general model built to process,
  understand and generate multiple modalities: text, images, video, audio.
- Each definition is short and correct; no extra invented model types.
- Reply grounded in the selected introduction deck.

### Record

- Actual prompt entered:
- Files selected:
- Files Fazah used:
- Result: Pass / Small Issue / Fail / Critical Fail
- Short note:

---

## Turn 2   (continue the same chat; keep `01_dvlm_introduction.pptx` selected)

### Enter

```text
so can a VLM generate images?
```

### Expect

- Says no per the deck: a VLM understands language and images but **generates text** — image
  generation is not part of the deck's VLM definition.
- Contrasts correctly with the MLLM, which is the one defined to generate multiple modalities
  (text, images, video, audio).
- Does not invent capabilities beyond the deck's definitions.

### Record

- Actual prompt entered:
- Files selected:
- Files Fazah used:
- Result: Pass / Small Issue / Fail / Critical Fail
- Short note:

---

## Turn 3   (continue the same chat; keep `01_dvlm_introduction.pptx` selected)

### Enter

```text
turn the definitions into a table
```

### Expect

- A table with three rows (LLM, VLM, MLLM) and columns along the lines of what each understands
  and what each generates, carried from Turns 1–2.
- Content matches the earlier turns (VLM = LLM + vision encoder, generates text; MLLM covers
  text, images, video, audio); nothing dropped or reworded into a wrong meaning.
- No fourth row or invented model type appears.

### Record

- Actual prompt entered:
- Files selected:
- Files Fazah used:
- Result: Pass / Small Issue / Fail / Critical Fail
- Short note:

---

## Turn 4   (continue the same chat; keep `01_dvlm_introduction.pptx` selected)

### Enter

```text
make a matching exercise from this — terms on one side, descriptions on the other
```

### Expect

- A matching exercise with the three terms (LLM, VLM, MLLM) in one column and their three
  descriptions in the other, shuffled so the pairs are not aligned.
- Descriptions are the deck's definitions, distinct enough to have exactly one right match each
  (e.g. "generates text only but also understands images" ↔ VLM).
- No answers/connecting lines shown in the exercise itself; still grounded in the intro deck.

### Record

- Actual prompt entered:
- Files selected:
- Files Fazah used:
- Result: Pass / Small Issue / Fail / Critical Fail
- Short note:

---

## Turn 5   (continue the same chat; keep `01_dvlm_introduction.pptx` selected)

### Enter

```text
gimme the answer key for the matching
```

### Expect

- A key mapping each term to its correct description, one-to-one, consistent with the exercise
  in Turn 4.
- Mapping is correct per the deck (LLM ↔ language-only; VLM ↔ LLM + vision encoder, text output;
  MLLM ↔ text/images/video/audio).
- The exercise itself is unchanged; no new items invented.

### Record

- Actual prompt entered:
- Files selected:
- Files Fazah used:
- Result: Pass / Small Issue / Fail / Critical Fail
- Short note:

---

## Turn 6   (continue the same chat; keep `01_dvlm_introduction.pptx` selected)

### Enter

```text
which file did all this come from
```

### Expect

- Fazah names `01_dvlm_introduction.pptx` (the introduction deck) as the source.
- No other file is claimed as a source for this material.
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
