# S013 — Auditor adds one instruction

## Tests

Fazah honors one auditor-added instruction on the opening turn and then carries the ethics content
through a multi-turn workflow — examples, student summary, a check, a student version, and source —
without losing the base content or the added constraint.

## Setup

- Start: New chat
- Select files: `Ch1 Introduction.pptx`
- Do not select: any other deck
- Turns: 6
- Auditor variation: Allowed — see the Auditor variation section

---

## Turn 1

### Enter

```text
explain software engineering ethics
```

(Then add exactly one instruction of your own — see the Auditor variation section.)

### Expect

- Explains SE ethics grounded in Ch1: engineers have wider responsibilities than technical skill,
  and ethics is more than obeying the law.
- Names the issues of professional responsibility: confidentiality, competence, intellectual
  property rights, computer misuse.
- Honors the one added instruction (format, length, audience, or example) while keeping the content correct.

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
add a real example for each of the 4 responsibilities
```

### Expect

- Gives one concrete example each for confidentiality, competence, IP rights, and computer misuse.
- Examples fit each responsibility correctly; the four responsibilities from turn 1 are preserved.
- Any instruction added in turn 1 (if a persistent one, e.g. audience) is still respected.

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
turn this into a short student summary
```

### Expect

- Produces a short, student-friendly summary of the four responsibilities and their examples.
- Content stays consistent with the earlier turns; nothing new or off-topic is introduced.

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
make a 3 question check on this
```

### Expect

- Produces exactly three questions covering the ethics responsibilities.
- Questions draw only on the content covered above.

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

## Turn 6   (continue the same chat)

### Enter

```text
which file did this come from
```

### Expect

- Names the Introduction deck (`Ch1 Introduction.pptx`) as the source.
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
- "Add one practical example."
- "Make it suitable for first-year students."
- "Keep it under 250 words."

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
