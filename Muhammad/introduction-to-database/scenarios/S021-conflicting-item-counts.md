# S021 — Conflicting item counts (10 vs exactly 15)

## Tests

A self-contradictory request — "10 questions" but "exactly 15 questions" — should be caught: Fazah
flags the conflict and clarifies rather than silently guessing, then — once resolved to 12 and Lec2
is selected — builds 12 conditionals questions from Lec2 with answers, a student version, and a count
confirmation.

## Setup

- Start: New chat
- Select files: none at first; select `Lec2.pdf` (IF / CASE) at Turn 3
- Do not select: any file until Turn 3
- Turns: 6
- Auditor variation: Not allowed

---

## Turn 1

### Enter

```text
make 10 questions and keep the assessment to exactly 15 questions
```

### Expect

- Detects the contradiction — 10 questions vs "exactly 15 questions" — and flags it, asking which
  count to use OR clearly stating one with a reason.
- Does not silently pick a number, split the difference, or average the two.
- No content generated from a guessed count; no invented source.

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
actually lets make it 12
```

### Expect

- Accepts 12 as the resolved count, superseding both 10 and 15.
- Confirms 12; since nothing is selected yet, may ask which file/topic to use.
- No fabricated content or source.

### Record

- Actual prompt entered:
- Files selected:
- Files Fazah used:
- Result: Pass / Small Issue / Fail / Critical Fail
- Short note:

---

## Turn 3  (continue the same chat — select `Lec2.pdf`)

### Enter

```text
ok produce the 12 questions on conditionals from this file
```

### Expect

- Produces exactly 12 questions on conditionals grounded in Lec2 — `IF` / `IF..ELSE` / `IF..ELSIF` /
  nested `IF` / `CASE` / searched `CASE`.
- The count is 12 (not 10 or 15); deck examples (grade bands, grade→text) are fine.
- Grounded in `Lec2.pdf`; no invented content.

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
add answers to all
```

### Expect

- The same 12 questions are kept; each gets a correct answer supported by Lec2.
- Answers stay within conditionals content (IF variants vs CASE).
- Still grounded in `Lec2.pdf`; still 12.

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

- The same 12 questions in a student-facing version with NO answers shown
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
confirm the count is 12
```

### Expect

- States there are exactly 12 questions, matching the Turn 2 resolution.
- Not 10 and not 15; the count is consistent with the produced set.

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
