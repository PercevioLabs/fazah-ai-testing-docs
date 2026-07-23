# S022 — "Same sources as before" in a fresh chat

## Tests

In a brand-new chat with no prior context, "use the same sources as before" has no referent; Fazah
must not invent or assume a prior source — it asks or says none is selected — then, once Lec3 is
selected, builds a loops quiz grounded in Lec3 with answers, a student version, and a source
confirmation.

## Setup

- Start: New chat (a fresh chat — no prior conversation, no selected files)
- Select files: none at first; select `Lec3.pdf` (loops) at Turn 2
- Do not select: any file at Turn 1 — there is deliberately no "before" to reference
- Turns: 6
- Auditor variation: Not allowed

---

## Turn 1

### Enter

```text
use the same sources as before and make a quiz
```

### Expect

- States there is no prior source/context in this new chat (nothing is selected) and asks which
  file(s) to use.
- Does not fabricate a "previous" source or generate a quiz from an assumed file.
- No invented content.

### Record

- Actual prompt entered:
- Files selected:
- Files Fazah used:
- Result: Pass / Small Issue / Fail / Critical Fail
- Short note:

---

## Turn 2  (continue the same chat — select `Lec3.pdf`)

### Enter

```text
use this one
```

### Expect

- Recognizes `Lec3.pdf` (loops) as the now-selected source and confirms it will use it.
- Does not treat it as the phantom "same as before" source.
- No fabricated content; may wait to generate until told.

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
ok make the quiz
```

### Expect

- Produces a quiz grounded in Lec3 — simple `LOOP`/`WHILE`/`FOR`, plus nested/reverse behavior per
  the deck.
- No invented constructs; keeps the deck's style (`mod`, counter loops).
- Grounded in `Lec3.pdf`; note the item count produced.

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
add answers
```

### Expect

- The same quiz questions are kept; each gets a correct answer supported by Lec3.
- Answers stay within loops content (simple/while/for, exit/counter/nested behavior).
- Still grounded in `Lec3.pdf`.

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
student version, no answers
```

### Expect

- The same questions in a student-facing version with NO answers shown
  (answer-leakage check — leaked answers = Critical fail).
- The teacher version with answers from Turn 4 is preserved; only the student copy is produced.

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
confirm which source this quiz used
```

### Expect

- Names `Lec3.pdf` as the source used.
- Does not claim a "same as before" source or any file that was never selected, and does not say it
  had no source.

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
