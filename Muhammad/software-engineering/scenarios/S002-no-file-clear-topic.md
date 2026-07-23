# S002 — No file selected, clear topic (auto source selection)

## Tests

With no file selected, Fazah auto-selects the correct course material from a clearly-scoped topic,
then sustains a multi-turn workflow — deepening one testing stage, tabulating a comparison, confirming
the source, and producing teacher and student questions — all without fabricating a source.

## Setup

- Start: New chat
- Select files: none
- Do not select: any deck (this scenario tests auto source selection)
- Turns: 6
- Auditor variation: Not allowed

---

## Turn 1

### Enter

```text
explain development testing, release testing & user testing
```

### Expect

- Fazah auto-selects/uses the Testing deck (`Ch4 Testing.pptx`) — grounding badge / Testing under
  used sources — even though no file was selected.
- Development testing = testing done by the team developing the system (unit / component / system);
  release testing = a separate team tests a release for use outside the dev team, usually black-box;
  user testing = users/customers test in their own environment (alpha / beta / acceptance).
- It does not invent or cite a source that does not exist.

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
go deeper on release testing, i want the black-box angle & who actually runs it
```

### Expect

- Builds on the Turn 1 answer rather than restarting.
- Release testing = usually a **black-box** process, run by a team separate from the developers; goal
  is to convince the supplier the system is good enough for use.
- Still grounded in the Testing deck.

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
now compare release testing vs user testing in a table
```

### Expect

- A table contrasting release testing and user testing (e.g. who runs it, environment, purpose).
- Release = separate dev-side team, black-box, "good enough to release"; user = users/customers in
  their own environment (alpha / beta / acceptance).
- Content stays within the Testing deck; no material pulled from other chapters.

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
which course file did all this come from
```

### Expect

- Fazah names the Testing deck (`Ch4 Testing.pptx`).
- It does not claim a file that does not exist and does not say it had no source.

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
make 3 review qs from that table w/ answers
```

### Expect

- Exactly three questions, drawn from the release-vs-user-testing comparison built above.
- Each has a correct answer supported by the Testing deck.

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
now a student version of those 3, no answers
```

### Expect

- The same three questions in a student-facing version with NO answers shown
  (answer-leakage check — leaked answers = Critical fail).
- The Turn 5 teacher version is preserved; only the student copy is produced.

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
