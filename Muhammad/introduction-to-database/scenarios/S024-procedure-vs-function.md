# S024 — Procedure vs function, compare then assess (auditor variation)

## Tests

With only the procedures & functions lecture selected, Fazah compares a procedure and a function on
the terms Lec6 uses (a function must return a value), then holds a conversational build — a fitting
case for each, a forgettable difference, a table, and teacher then student questions — all grounded
in Lec6, without fabricating verbatim example code from the deck's image slides.

## Setup

- Start: New chat
- Select files: `Lec6.pdf` (procedures & functions)
- Do not select: any other lecture
- Turns: 7
- Auditor variation: Allowed (see the Auditor variation section)

---

## Turn 1

### Enter

```text
ok so can u compare a procedure and a function for me
```

### Expect

- States the key difference: a **function must return a value**, a procedure need not — per Lec6.
- Frames both as subprograms that package block logic (procedure performs a task; function is the
  same but returns a value).
- Grounded in the selected lecture (grounding badge / Lec6 under used sources), not a generic answer.

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
gimme one realistic case where each fits, staying within how the lecture frames them
```

### Expect

- One fitting use for a procedure (perform a task, e.g. update/insert, value returned via `OUT` if any)
  and one for a function (compute and `RETURN` a value) — framed as Lec6 frames them (IN/OUT/IN OUT).
- No features beyond the deck (no packages, triggers, etc.).
- Because Lec6's worked examples are image slides, it does not fabricate verbatim example code and
  attribute it to the deck.

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
add one key difference i might forget
```

### Expect

- Adds a real Lec6 detail: a procedure has **no `DECLARE` keyword** (vars go after `IS`/`AS`), or
  **no data size in the declaration**, or a function **needs `RETURN DATATYPE` plus a return variable**.
- Keeps the earlier comparison; extends rather than rewrites.
- Still grounded in `Lec6.pdf`.

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
cool now put it in a table
```

### Expect

- A table contrasting procedure vs function on the points built up (returns a value, `RETURN` clause,
  `DECLARE` keyword / no size in declarations).
- No new claims added; only reformatted.
- Still grounded in `Lec6.pdf`.

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
ok make 4 questions from this
```

### Expect

- Exactly 4 questions on procedure vs function, drawn from the material above, not new topics.
- Any answers given are consistent with Lec6 (function must return; IN/OUT/IN OUT modes; no `DECLARE`
  keyword).
- Still grounded in `Lec6.pdf`.

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
and a student version, no answers
```

### Expect

- The same 4 questions, student-facing, with NO answers shown
  (answer-leakage check — leaked answers = Critical fail).
- The teacher version from Turn 5 is preserved; only the student copy is produced.

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
which file did u pull this from
```

### Expect

- Names `Lec6.pdf` (procedures & functions) as the source used throughout.
- Does not claim a lecture that was never selected, and does not hedge that it had no source.

### Record

- Actual prompt entered:
- Files selected:
- Files Fazah used:
- Result: Pass / Small Issue / Fail / Critical Fail
- Short note:

---

## Auditor variation

The auditor may vary the *phrasing or a single formatting ask* without breaking the Expect lines. Any
one of these substitutions is acceptable:

- Turn 4 ("put it in a table") may instead be "add a limitation" / "add a constraint of each".
- Turn 2's framing may be narrowed to "for first-year students" or "keep it under 200 words".
- Any follow-up may be reworded conversationally, as long as the underlying request (compare /
  realistic case / forgettable difference / table / 4 questions / student version / which file) is
  preserved.

Do not vary: the target of 7 turns, the no-answers student turn, or the which-file turn. All Expect
lines still apply under any allowed substitution.

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
