# S037 — Cursor quiz quality refinement

## Tests

Fazah builds a 12-MCQ quiz on the explicit-cursor lecture, then quality-refines it — de-duplicating,
strengthening distractors, converting the tail to trace/scenario items, and self-checking one correct
answer per MCQ — before splitting student/teacher versions and extending the set, all grounded in the
same lecture.

## Setup

- Start: New chat
- Select files: `Lec5.pdf` (explicit cursors)
- Do not select: any other lecture
- Turns: 11
- Auditor variation: Not allowed

---

## Turn 1

### Enter

```text
make 12 mcqs covering the whole explicit-cursor lecture
```

### Expect

- Exactly 12 MCQs spanning Lec5 (four-step lifecycle, `%FOUND`/`%NOTFOUND`/`%ROWCOUNT`, fetch-loop
  styles).
- Each MCQ has options with a correct answer; content stays within the deck (HR `employees` example).
- Grounded in `Lec5.pdf` (grounding badge / Lec5 under used sources).

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
find and replace any duplicate questions
```

### Expect

- Identifies duplicate / near-duplicate MCQs and replaces them with distinct ones; still exactly 12.
- Replacements stay on Lec5 topics; no content loss elsewhere.
- Grounded in Lec5.

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
improve the weak distractors
```

### Expect

- Strengthens weak / implausible distractors while keeping one correct answer per MCQ.
- Question count (12) and correct answers preserved.
- Grounded in Lec5; distractors plausible within the deck.

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
make the last 3 trace/scenario based
```

### Expect

- Questions 10–12 become trace / scenario-based (e.g. predict `%ROWCOUNT` or fetch-loop behavior);
  still 12 total.
- The first 9 are preserved; correct answers consistent with Lec5.
- Grounded in Lec5.

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
check exactly one answer is correct per mcq
```

### Expect

- Verifies each of the 12 MCQs has exactly one correct option and reports any that don't.
- No content rewritten except to fix a multi-correct or zero-correct item.
- Grounded in Lec5.

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
student version without answers
```

### Expect

- Student version of all 12 MCQs with NO correct answers marked (answer-leakage check — leaked
  answers = Critical fail).
- Options preserved; the teacher version is not destroyed.
- Grounded in Lec5.

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
teacher key with explanations
```

### Expect

- Teacher key marking the correct option per MCQ with a short explanation each.
- Explanations consistent with Lec5; the student version stays answer-free.
- Grounded in Lec5.

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
add 2 more on the cursor for loop, keep the original 12
```

### Expect

- Adds 2 new MCQs on the cursor `FOR` loop (`FOR emp_rec IN emp_cur LOOP` — auto open/fetch/close);
  total now 14.
- The original 12 are kept intact.
- Grounded in Lec5.

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
reorder by subtopic
```

### Expect

- Reorders the 14 MCQs grouped by subtopic (lifecycle / attributes / loop styles); no question
  dropped or altered.
- Still 14 with one correct answer each.
- Grounded in Lec5.

### Record

- Actual prompt entered:
- Files selected:
- Files Fazah used:
- Result: Pass / Small Issue / Fail / Critical Fail
- Short note:

---

## Turn 10  (continue the same chat)

### Enter

```text
label each question with its subtopic
```

### Expect

- Adds a subtopic label to each of the 14 MCQs (e.g. Lifecycle, Attributes, FOR loop).
- Labels match Lec5 subtopics; no question content changed.
- Grounded in Lec5.

### Record

- Actual prompt entered:
- Files selected:
- Files Fazah used:
- Result: Pass / Small Issue / Fail / Critical Fail
- Short note:

---

## Turn 11  (continue the same chat)

### Enter

```text
which file + confirm every mcq still has exactly one correct answer
```

### Expect

- Names `Lec5.pdf` as the source used; does not claim an unselected file.
- Confirms all 14 MCQs have exactly one correct answer each.
- Consistent with the running set.

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
