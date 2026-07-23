# S032 — Requirements teaching deck with slide-specific edits, then handout

## Tests

Sustained multi-turn workflow on ONE eight-slide requirements deck: Fazah applies targeted per-slide
edits (simplify, comparison table, scenario, speaker notes), grows it with a title and agenda slide and
a summary, then derives a student handout — changing only the targeted slide each time and preserving
prior edits as slides are renumbered.

## Setup

- Start: New chat
- Select files: `Ch3 Req Eng.pptx`
- Do not select: any other deck
- Turns: 10
- Auditor variation: Allowed — see the Auditor variation section

---

## Turn 1

### Enter

```text
Create an eight-slide teaching deck on requirements engineering.
```

### Expect

- Exactly eight slides are produced.
- Content is grounded in the Requirements deck (e.g. functional vs. non-functional requirements,
  NFR classifications, elicitation techniques, validation checks), not generic material.
- Slides are numbered/ordered so later slide-specific edits can be targeted.

### Record

- Actual prompt entered:
- Files selected:
- Files Fazah used:
- Result: Pass / Small Issue / Fail / Critical Fail
- Short note:

---

## Turn 2   (continue the same chat; keep `Ch3 Req Eng.pptx` selected)

### Enter

```text
Make slide 2 simpler.
```

### Expect

- Only slide 2 is simplified.
- Slides 1 and 3–8 are unchanged.
- The change is a new version of the same eight-slide deck.

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
Turn slide 4 into a comparison table.
```

### Expect

- Only slide 4 becomes a comparison table (e.g. functional vs. non-functional).
- The other seven slides are unchanged, including the simplified slide 2.
- The deck still has eight slides.

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
Add a scenario to slide 6.
```

### Expect

- Only slide 6 gains a scenario (e.g. a Mentcare or iLearn example from the deck).
- The other seven slides are unchanged, including edits from earlier turns.
- The deck still has eight slides.

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
Add speaker notes without changing the slide text.
```

### Expect

- Speaker notes are added for the slides.
- The visible slide text is unchanged from the prior version.
- All earlier slide-specific edits (slides 2, 4, 6) are still present.

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
Add a title slide at the front.
```

### Expect

- A title slide is prepended; the deck now has nine slides.
- The earlier edits move with their content (the simplified slide, comparison table, and scenario
  survive under their new numbers).
- Speaker notes from Turn 5 are retained.

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
Add an agenda slide after the title.
```

### Expect

- An agenda slide is inserted after the title; the deck now has ten slides.
- The agenda reflects the deck's actual topics (grounded in the Requirements content).
- All prior edits and speaker notes are preserved under their new positions.

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
Make the last slide a summary.
```

### Expect

- Only the final slide becomes a summary of the deck's key points.
- The comparison table, scenario, and other edited slides are unchanged.
- Slide count is unchanged by this edit (still ten).

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
Make a student handout from the deck.
```

### Expect

- A student handout is derived from the deck, written for students.
- Speaker notes / teacher-only asides are not carried into the handout (audience-leakage check).
- The handout content matches the current deck's slides.

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
Which file did you use for all of this?
```

### Expect

- Fazah names `Ch3 Req Eng.pptx` as the source.
- It does not claim any other deck; all content traces to the Requirements material.
- The answer reflects the actual deck and handout produced.

### Record

- Actual prompt entered:
- Files selected:
- Files Fazah used:
- Result: Pass / Small Issue / Fail / Critical Fail
- Short note:

---

## Auditor variation

Add or change one realistic instruction. Record exactly what you entered. Do not change the
scenario's main goal (a requirements deck refined by slide-specific edits).

- Change the slide count at Turn 1 (e.g. a ten-slide deck).
- Target first-year students.
- Ask for the title slide before the simplify edit, changing the numbering order.
- Make the agenda slide bullet the deck's four validation checks.

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
