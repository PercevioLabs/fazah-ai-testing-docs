# S015 — Dense assessment constraints, loops lecture

## Tests

With the loops lecture selected, Fazah builds a tightly-constrained 8-MCQ quiz, then edits distractors,
converts items to trace-the-output, verifies single correct answers, grows to 10, reorders, and splits
student/teacher versions — holding every constraint and staying grounded in Lec3.

## Setup

- Start: New chat
- Select files: `Lec3.pdf` (loops: simple / while / for / nested / reverse)
- Do not select: any other lecture
- Turns: 9
- Auditor variation: Not allowed

---

## Turn 1

### Enter

```text
make a quiz from the loops lecture: exactly 8 MCQs, medium, exactly one correct answer, answers included, one-sentence explanations, cover simple loop / while / for / nested / reverse
```

### Expect

- Exactly 8 MCQs, medium difficulty, each with exactly one correct answer and a one-sentence
  explanation.
- Covers simple `LOOP`, `WHILE`, `FOR`, nested loops, and reverse — all grounded in Lec3.
- Grounded in `Lec3.pdf`; no fabricated loop constructs.

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
replace only the weakest distractors
```

### Expect

- Only weak distractor options are revised; the questions and correct answers are otherwise preserved.
- Still 8 MCQs, still Lec3 loop content.

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
make the last 2 trace-the-output based
```

### Expect

- Questions 7 and 8 become trace-the-output items (e.g. a nested loop printing `i||j`, or reverse
  counting) — consistent with Lec3 examples.
- Each still has exactly one correct answer.

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
check each has exactly one correct answer
```

### Expect

- Verifies all 8 questions have exactly one correct option; fixes any that violate this.
- Reports the check clearly; no answers leaked.

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
add 2 more to make 10, still medium
```

### Expect

- 2 new medium MCQs added → 10 total, still Lec3 loop content.
- The prior 8 questions are preserved.

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
reorder easiest to hardest
```

### Expect

- The 10 questions reordered easiest → hardest; none dropped or added.
- Question content unchanged — only order.

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
student version, no answers
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

## Turn 8  (continue the same chat)

### Enter

```text
teacher key w explanations
```

### Expect

- A teacher key: all 10 correct answers with one-sentence explanations, grounded in Lec3.
- Consistent with the student version's questions.

### Record

- Actual prompt entered:
- Files selected:
- Files Fazah used:
- Result: Pass / Small Issue / Fail / Critical Fail
- Short note:

---

## Turn 9  (continue the same chat)

### Enter

```text
confirm it covers all the loop types
```

### Expect

- Confirms coverage of simple `LOOP`, `WHILE`, `FOR`, nested, and reverse across the 10 questions.
- Grounded in Lec3; names `Lec3.pdf` if it references the source.

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
