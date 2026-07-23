# S025 — Functional vs non-functional requirements

## Tests

With only the Requirements deck selected, Fazah sustains one workflow: it distinguishes functional
and non-functional requirements, gives Mentcare-style examples, builds a student self-check plus a
teacher key, adds the three NFR classifications and a matching question, and confirms its source —
retaining context across all turns.

## Setup

- Start: New chat
- Select files: `Ch3 Req Eng.pptx`
- Do not select: any other deck
- Turns: 8
- Auditor variation: Not allowed

---

## Turn 1

### Enter

```text
whats the diff between functional and non-functional requirements
```

### Expect

- Functional requirements = statements of services the system should provide / how it reacts to
  inputs / how it behaves in situations.
- Non-functional requirements = constraints on services or functions (timing, standards, process),
  often apply to the system as a whole, and may be more critical than functional ones.
- Grounded in the selected Requirements deck (badge / Requirements under used sources).

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
ok now a mentcare style example of each
```

### Expect

- Functional example matches the deck (e.g. search appointment lists for all clinics / daily
  per-clinic patient list / staff identified by an 8-digit employee number).
- Non-functional example matches the deck (e.g. availability Mon–Fri 08:30–17:30 with downtime ≤5s/day;
  identity-card authentication; HStan-03-2006-priv privacy provision).
- Examples stay Mentcare-grounded and build on the Turn 1 distinction.

### Record

- Actual prompt entered:
- Files selected:
- Files Fazah used:
- Result: Pass / Small Issue / Fail / Critical Fail
- Short note:

---

## Turn 3   (continue the same chat; keep `Ch3 Req Eng.pptx` selected)

### Enter

```text
turn this into a short student self-check
```

### Expect

- A short student-facing self-check on functional vs non-functional requirements that builds on the
  prior two turns.
- Any answers are clearly separated/labelled as self-check answers, not mixed into the questions.
- Content stays course-grounded (Mentcare-flavoured), not generic.

### Record

- Actual prompt entered:
- Files selected:
- Files Fazah used:
- Result: Pass / Small Issue / Fail / Critical Fail
- Short note:

---

## Turn 4   (continue the same chat; keep `Ch3 Req Eng.pptx` selected)

### Enter

```text
now make a teacher key for the self-check
```

### Expect

- A teacher key with correct answers for each self-check item from Turn 3.
- Answers are correct against the deck (correctly classify FR vs NFR, correct Mentcare examples).
- The key matches the same items/count as the self-check; no new questions invented.

### Record

- Actual prompt entered:
- Files selected:
- Files Fazah used:
- Result: Pass / Small Issue / Fail / Critical Fail
- Short note:

---

## Turn 5   (continue the same chat; keep `Ch3 Req Eng.pptx` selected)

### Enter

```text
ok now a student version, no answers
```

### Expect

- The same self-check items, with all answers/keys removed.
- No answer leaks into the student version (answers leaking = Critical fail).
- Item count and topics are unchanged from Turns 3–4.

### Record

- Actual prompt entered:
- Files selected:
- Files Fazah used:
- Result: Pass / Small Issue / Fail / Critical Fail
- Short note:

---

## Turn 6   (continue the same chat; keep `Ch3 Req Eng.pptx` selected)

### Enter

```text
add the 3 non-functional requirement classifications from the deck
```

### Expect

- Names the three NFR classifications per Chapter 4/Requirements deck: **product**, **organisational**,
  **external**.
- Ties them to the Mentcare NFR examples where sensible (downtime ≤5s/day = product; identity-card
  authentication = organisational; HStan-03-2006-priv privacy = external).
- Extends the earlier material without discarding the self-check/key already built.

### Record

- Actual prompt entered:
- Files selected:
- Files Fazah used:
- Result: Pass / Small Issue / Fail / Critical Fail
- Short note:

---

## Turn 7   (continue the same chat; keep `Ch3 Req Eng.pptx` selected)

### Enter

```text
add one more question on the NFR types
```

### Expect

- One additional question specifically on the product/organisational/external classifications.
- The new question is added to the existing set (not a wholesale replacement of prior questions).
- Question is answerable from the deck's NFR classification content.

### Record

- Actual prompt entered:
- Files selected:
- Files Fazah used:
- Result: Pass / Small Issue / Fail / Critical Fail
- Short note:

---

## Turn 8   (continue the same chat; keep `Ch3 Req Eng.pptx` selected)

### Enter

```text
which file did all this come from
```

### Expect

- Fazah names `Ch3 Req Eng.pptx` (the Requirements deck) as the source.
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

For the complete workflow, see [Context Diagram](../misc/CONTEXT-DIAGRAM.md).
