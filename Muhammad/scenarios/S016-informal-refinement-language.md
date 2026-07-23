# S016 — Informal refinement language

## Tests

Fazah resolves informal references across many turns and preserves the same Scrum definition while
refining it — simplify, add an analogy, condense, add questions, produce a student version, and
report the source — never rewriting the definition it was told to keep.

## Setup

- Start: New chat
- Select files: none
- Do not select: n/a
- Turns: 7
- Auditor variation: Allowed — see the Auditor variation section

---

## Turn 1

### Enter

```text
explain scrum
```

### Expect

- Gives a correct Scrum explanation, course-consistent with the Agile deck (e.g. sprints, product
  backlog, product owner, ScrumMaster, daily Scrum).
- Answer is coherent and usable as a baseline for the next turns.

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
make it way simpler
```

### Expect

- Produces a simpler version of the same Scrum explanation.
- The core concepts / definition from turn 1 are preserved — only the language is simplified.
- Does not switch topics or drop the key ideas.

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
now give one real classroom-style analogy but dont change the definition
```

### Expect

- Adds exactly one real, classroom-style analogy for Scrum.
- The Scrum definition from the earlier turns is left unchanged.
- Only the analogy is added; nothing else is rewritten.

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
make it a four-line summary
```

### Expect

- Condenses to a four-line summary of Scrum.
- The definition and key ideas from earlier turns are kept — just shortened, not changed.

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
add 3 quick qs
```

### Expect

- Adds exactly three short questions about Scrum, drawn from what was covered.
- The four-line summary above is preserved; questions are appended, not a rewrite.

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
keep the definition but gimme a student version
```

### Expect

- Produces a student version of the three questions with NO answers shown.
- Answer leakage into the student version = Critical fail.
- The Scrum definition is kept intact, as instructed.

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
what source is this?
```

### Expect

- Points to the Agile deck (`Ch5 Agile SW Dev.pptx`) as where Scrum is covered.
- No source was selected, so it is honest about drawing on course-consistent knowledge / that deck —
  it does not fabricate a specific file it never used.

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

- "make it shorter" as the turn 2 refinement.
- Change the analogy domain in turn 3 (e.g. ask for a sports analogy).
- Ask for one concrete example instead of / alongside the analogy.
- Limit an answer to one paragraph.

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
