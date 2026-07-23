# S014 — Auditor writes the prompt

## Tests

Fazah is robust to realistic, self-composed human wording on the opening turn and then sustains the
same beginner-Scrum goal across follow-ups — analogy, roles, questions, student version, source —
still meeting the underlying goal regardless of the exact phrasing.

## Setup

- Start: New chat
- Select files: `Ch5 Agile SW Dev.pptx`
- Do not select: any other deck
- Turns: 6
- Auditor variation: Allowed — see the Auditor variation section

---

## Turn 1

### Enter

There is no fixed prompt for this scenario. You compose the wording yourself.

Goal: Ask Fazah to explain Scrum using the Agile lecture, for students who have never seen Scrum
before. Write your own natural prompt in your own words, then record exactly what you typed.

### Expect

- Explains Scrum grounded in the Agile deck (`Ch5 Agile SW Dev.pptx`): e.g. sprints, product backlog,
  product owner, ScrumMaster, daily Scrum.
- Pitched for beginners (plain language, defines terms rather than assuming prior knowledge).
- Content is correct regardless of the exact natural wording you chose.

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
can u add a simple analogy so beginners can picture it
```

### Expect

- Adds one simple analogy for Scrum without changing the definition from turn 1.
- Analogy is beginner-appropriate and does not misrepresent the Scrum concepts.

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
ok now list the key roles plainly - product owner, scrummaster n the dev team
```

### Expect

- Describes each of the three roles in plain language, grounded in the Agile deck.
- Roles are consistent with the earlier explanation; nothing contradicts turn 1.

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
make 4 beginner qs on this
```

### Expect

- Produces exactly four beginner-level questions about Scrum (roles, sprint, backlog, daily Scrum).
- Questions match the beginner audience and draw only on what was covered.

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
now gimme a student version of those questions
```

### Expect

- Produces the four questions with NO answers shown (student version).
- Answer leakage into the student version = Critical fail.
- Same four questions as turn 4.

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
confirm which file u used
```

### Expect

- Names the Agile deck (`Ch5 Agile SW Dev.pptx`) as the source.
- Does not claim any other or non-existent file.

### Record

- Actual prompt entered:
- Files selected:
- Files Fazah used:
- Result: Pass / Small Issue / Fail / Critical Fail
- Short note:

---

## Auditor variation

Add or change one realistic instruction. Record exactly what you entered. Do not change the
scenario's main goal.

Example variations:

- Change the student audience on Turn 1 (e.g. "for a high-school class" instead of undergraduates).
- Add "keep it under one minute to read" to Turn 1.
- Ask for one analogy on Turn 2 in a specific domain (e.g. sports or cooking).
- Use a more formal tone throughout.

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
