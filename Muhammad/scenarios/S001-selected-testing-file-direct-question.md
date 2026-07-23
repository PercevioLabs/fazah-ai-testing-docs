# S001 — Selected Testing file, direct concept question

## Tests

With only the Testing deck selected, Fazah answers a direct concept question grounded in that file,
then sustains a multi-turn workflow — deepening the distinction, adding examples, and turning it into
teacher and student assessment — all grounded in the same Testing deck.

## Setup

- Start: New chat
- Select files: `Ch4 Testing.pptx`
- Do not select: any other deck
- Turns: 6
- Auditor variation: Not allowed

---

## Turn 1

### Enter

```text
whats the difference between verification and validation
```

### Expect

- Verification = "are we building the product **right**?" (conforms to specification); validation =
  "are we building the **right** product?" (does what the user really requires) — matching the slides.
- The reply is grounded in the selected Testing deck (grounding badge / Testing under used sources),
  not a generic web answer.
- No invented citation to a chapter or file that was not selected.

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
add the inspections vs testing distinction to that
```

### Expect

- The prior verification/validation distinction is kept and extended (not rewritten from scratch).
- Inspections = static verification (examine the static representation, no execution, usable before
  implementation); testing = dynamic verification (exercise and observe behavior with test data).
- Still grounded in the Testing deck; presented as complementary, not opposing.

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
gimme one weather-station or Mentcare example for each of those 4 terms
```

### Expect

- One concrete example per term (verification, validation, inspections, testing), drawn from the
  weather-station or Mentcare material that the Testing deck actually contains.
- Examples stay consistent with the deck (e.g. weather-station object/state testing, Mentcare
  allergy/requirements-based tests); no example is fabricated and attributed to the deck.

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
ok turn all this into 4 short quiz qs w/ answers
```

### Expect

- Exactly four questions, covering the verification/validation/inspections/testing material built up
  above (not new topics).
- Each question has a correct answer supported by the Testing deck.
- Still grounded in `Ch4 Testing.pptx`.

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
now a student version of those 4, no answers
```

### Expect

- The same four questions appear in a student-facing version with NO answers shown
  (answer-leakage check — leaked answers = Critical fail).
- The teacher version from Turn 4 is preserved as its own version; only the student copy is produced.

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
which course file did you use for all this
```

### Expect

- Fazah names the Testing deck (`Ch4 Testing.pptx`) as the source used throughout.
- It does not claim any file that was never selected, and does not hedge that it had no source.

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
