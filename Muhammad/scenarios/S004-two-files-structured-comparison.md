# S004 — Two files selected, structured comparison table

## Tests

With two files selected, Fazah synthesizes a comparison table drawn only from those two sources, then
sustains a workflow — extending the table, condensing it to a slide, and generating teacher and
student questions — never pulling from the three unselected decks.

## Setup

- Start: New chat
- Select files: `Ch2 SW Processes.pptx` + `Ch5 Agile SW Dev.pptx`
- Do not select: `Ch1 Introduction.pptx`, `Ch3 Req Eng.pptx`, `Ch4 Testing.pptx`
- Turns: 7
- Auditor variation: Not allowed

---

## Turn 1

### Enter

```text
compare plan-driven, incremental & agile development in a table. include when each is most appropriate + one limitation of each, use only the selected slides
```

### Expect

- A table with all three approaches, each with a "when most appropriate" cell and one limitation
  (e.g. plan-driven suits stable, well-understood requirements but resists change; incremental gives
  faster delivery but reduced visibility / degrading structure; agile embraces change but keeps
  minimal documentation).
- Grounded in the Processes and Agile decks only; no requirements/testing/Ch1 material.
- Both selected files appear in "Sources used".

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
add a row for how much documentation each approach expects
```

### Expect

- One new row added; the existing three columns/rows from Turn 1 are preserved.
- Documentation levels are deck-consistent: plan-driven = planned/extensive documentation;
  incremental = reduced process visibility / documents may lag; agile = minimal documentation
  ("working software over comprehensive documentation").

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
add one real project example for each approach
```

### Expect

- One example per approach, staying consistent with the two decks (e.g. plan-driven → large
  systems-engineering / critical systems with stable requirements; agile → evolving business/custom
  software).
- If the decks do not name a specific commercial product, Fazah uses a deck-consistent project *type*
  or notes the slides give none — it does not fabricate a named project and attribute it to the decks.

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
condense that whole table into a one-slide summary
```

### Expect

- A single compact slide capturing the three approaches and their key contrasts from the built-up
  table (not new content).
- Substance of the prior rows (appropriateness, limitation, documentation, example) is preserved in
  condensed form.

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
make 4 quiz qs from the table w/ answers
```

### Expect

- Exactly four questions, drawn from the plan-driven/incremental/agile comparison.
- Each has a correct answer supported by the two selected decks.

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
now a student version of those 4, no answers
```

### Expect

- The same four questions in a student-facing version with NO answers shown
  (answer-leakage check — leaked answers = Critical fail).
- The Turn 5 teacher version is preserved.

### Record

- Actual prompt entered:
- Files selected:
- Files Fazah used:
- Result: Pass / Small Issue / Fail / Critical Fail
- Short note:

---

## Turn 7  (continue the same chat)

### Enter

```text
confirm you only used the 2 decks i selected
```

### Expect

- Fazah confirms the sources were `Ch2 SW Processes.pptx` and `Ch5 Agile SW Dev.pptx` only.
- It does not claim to have used any of the three unselected decks.

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
