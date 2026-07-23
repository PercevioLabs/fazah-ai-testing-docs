# S003 — Wrong file selected for the topic (conflict, then recovery)

## Tests

When the selected file does not support the requested topic, Fazah honestly flags the gap instead of
fabricating content, then — across a sustained workflow — recovers onto the right material and builds
the full functional-vs-non-functional lesson and assessment from it.

## Setup

- Start: New chat
- Select files: `Ch5 Agile SW Dev.pptx` only
- Do not select: `Ch3 Req Eng.pptx` (the correct source — auditor withholds it until Turn 3)
- Turns: 8
- Auditor variation: Not allowed

---

## Turn 1  (Agile deck selected)

### Enter

```text
explain functional & non-functional requirements from the selected slides
```

### Expect

- Fazah recognizes the selected Agile deck does NOT cover functional vs non-functional requirements
  and says so honestly (one-line gap note), rather than blocking.
- It offers/asks to use the Requirements material, or proceeds only with a clear caveat that the
  content is not from the selected file.
- It does NOT fabricate FR/NFR content attributed to the Agile deck. (Fabricated FR/NFR content
  claimed to be from the Agile deck = Critical fail.)

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
hmm ok so which file should i use for this then
```

### Expect

- Fazah points to the Requirements material (`Ch3 Req Eng.pptx`) as the right source for functional
  vs non-functional requirements.
- It does not invent a filename; it references the actual course deck.

### Record

- Actual prompt entered:
- Files selected:
- Files Fazah used:
- Result: Pass / Small Issue / Fail / Critical Fail
- Short note:

---

## Turn 3  (before entering: select `Ch3 Req Eng.pptx`; continue the same chat)

### Enter

```text
ok use this Requirements file instead
```

### Expect

- Fazah switches to the Requirements deck; used sources now reflect `Ch3 Req Eng.pptx`.
- It confirms the source change without re-asking what the topic is (the goal is unchanged).

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
now explain functional vs non-functional requirements properly from it
```

### Expect

- Functional requirements = statements of services the system should provide / how it reacts to
  inputs / how it behaves (may state what it should not do); non-functional = constraints on services
  or functions (timing, standards, quality), often applying to the system as a whole.
- Grounded in the Requirements deck, not the Agile deck.

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
gimme a Mentcare example of each
```

### Expect

- A functional Mentcare example (e.g. search appointment lists / daily per-clinic patient list /
  8-digit employee-number identification) and a non-functional Mentcare example (e.g. availability
  Mon–Fri 08:30–17:30 with downtime ≤5s/day, or the privacy/authentication provisions).
- Examples are from the Requirements deck's Mentcare material, not fabricated.

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
put functional vs non-functional into a comparison table
```

### Expect

- A table contrasting the two, reusing the definitions and Mentcare examples built above (not new
  material).
- Still grounded in the Requirements deck.

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
make 5 questions from that table for students, no answers shown
```

### Expect

- Exactly five questions derived from the comparison table.
- Student-facing version with NO answers shown (answer-leakage check — leaked answers = Critical fail).

### Record

- Actual prompt entered:
- Files selected:
- Files Fazah used:
- Result: Pass / Small Issue / Fail / Critical Fail
- Short note:

---

## Turn 8  (continue the same chat)

### Enter

```text
confirm the source, which file did these questions come from
```

### Expect

- Fazah names the Requirements deck (`Ch3 Req Eng.pptx`), not the Agile deck.
- It does not credit the original (wrong) Agile selection for the FR/NFR content.

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
