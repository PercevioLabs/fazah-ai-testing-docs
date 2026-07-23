# S010 — Typo-heavy conditional-statements quiz build

## Tests

With the conditionals lecture selected, Fazah reads past heavy typos and txt-speak, builds a 10-MCQ
IF/CASE quiz, and holds the count and constraints through hardening, reordering, student/teacher
versions, and a scenario-question edit — all grounded in Lec2.

## Setup

- Start: New chat
- Select files: `Lec2.pdf` (IF / CASE)
- Do not select: any other lecture
- Turns: 8
- Auditor variation: Not allowed

---

## Turn 1

### Enter

```text
make 10 mcq frm conditionls (if n case) hard w answrs n short explaination
```

### Expect

- Exactly 10 MCQs on conditionals (IF and CASE), hard, each with an answer and a short explanation.
- Grounded in Lec2: IF / IF..ELSE / IF..ELSIF, nested IF, CASE, searched CASE, grade-band examples.
- Grounded in `Lec2.pdf`; no fabricated constructs beyond the deck.

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
q4 too ez make it hardr
```

### Expect

- Question 4 revised to be harder; still an IF/CASE MCQ from Lec2.
- The other 9 questions preserved; still 10 total.
- Still grounded in `Lec2.pdf`.

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
reordr esiest to hardst
```

### Expect

- The same 10 questions reordered easiest → hardest; none dropped or added.
- Question content unchanged — only order.

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
make studnt version no answrs
```

### Expect

- The same 10 questions, student-facing, with NO answers or explanations shown
  (answer-leakage check — leaked answers = Critical fail).
- The teacher version is preserved.

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
teachr key w explanations
```

### Expect

- A teacher key: all 10 with correct answers and short explanations, matching Lec2.
- Consistent with the student version's questions from Turn 4.

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
add 2 scenario qs bout CASE keep 10 total
```

### Expect

- Adds 2 scenario/applied CASE questions but the total stays 10 (so 2 are replaced) — honors both
  "add 2" and "keep 10 total".
- CASE content grounded in Lec2 (selector CASE / searched CASE).

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
chek only 1 ans is corect each
```

### Expect

- Verifies each of the 10 MCQs has exactly one correct option; flags or fixes any with zero or more
  than one.
- Reports the check clearly; no answers leaked into any student-facing copy.

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
wich file did u use
```

### Expect

- Names `Lec2.pdf` (conditionals) as the source used throughout.
- Does not claim a lecture that was never selected.

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
