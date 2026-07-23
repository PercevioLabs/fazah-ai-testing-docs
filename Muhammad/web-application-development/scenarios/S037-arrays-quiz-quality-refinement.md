# S037 — Arrays quiz quality refinement

## Tests

With only the arrays deck selected, Fazah builds a 12-question MCQ quiz and then, across 22 iterative
turns, refines its quality — de-duplicating, strengthening distractors, enforcing exactly one correct
answer per item, converting some to scenario/write-code, splitting a clean student version from a
teacher key, and adding subtopic coverage — all grounded in php_arrays without answer leakage.

## Setup

- Start: New chat
- Select files: `php_arrays_presentation.pptx`
- Do not select: any other deck
- Turns: 22
- Auditor variation: Not allowed

---

## Turn 1

### Enter

```text
make 12 mcqs covering the whole arrays deck
```

### Expect

- Exactly 12 multiple-choice questions spanning the arrays deck (indexed, associative, multidimensional, create/access/update/foreach).
- Each item has one correct answer supported by php_arrays; grounded in the selected deck only.

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
find + replace any duplicate questions
```

### Expect

- Any near-duplicate items are identified and replaced with distinct ones; still 12, still grounded.

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

- Weak/implausible distractors are strengthened so each remains plausible but wrong; correct answers unchanged.
- Still 12, still one correct each.

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
make the last 3 scenario / write-code
```

### Expect

- Only the last 3 items become scenario or write-code questions (valid PHP array code); the first 9 stay MCQ.
- Still 12, grounded.

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
check theres exactly one correct answer per mcq
```

### Expect

- Confirms each MCQ has exactly one correct option (no zero-correct or multi-correct items).

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
student version, no answers
```

### Expect

- The same items as a student-facing version with NO correct options marked and no answers shown
  (answer-leakage check — leaked answers = Critical fail).

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
teacher key w explanations
```

### Expect

- A teacher key with the correct answer + a short explanation for each item, grounded in php_arrays.
- Student version stays answer-free.

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
add 2 on associative arrays but keep it at 12 total
```

### Expect

- Adds 2 associative-array questions while holding the total at 12 (2 weaker items swapped out).
- Associative facts match the deck (named keys, `"brand" => "Ford"`).

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
reorder by subtopic — indexed then associative then multidimensional
```

### Expect

- The 12 items reordered/grouped by subtopic in that order; none added or dropped.

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
label each subtopic
```

### Expect

- Each group labelled with its subtopic (indexed / associative / multidimensional / foreach).

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
which file did u use + confirm still one correct each
```

### Expect

- Names `php_arrays_presentation.pptx` as the source; does not claim an unselected deck (false claim = Critical fail).
- Confirms every MCQ still has exactly one correct answer.

### Record

- Actual prompt entered:
- Files selected:
- Files Fazah used:
- Result: Pass / Small Issue / Fail / Critical Fail
- Short note:

---

## Turn 12  (continue the same chat)

### Enter

```text
verify its still 12
```

### Expect

- Confirms exactly 12 questions.

### Record

- Actual prompt entered:
- Files selected:
- Files Fazah used:
- Result: Pass / Small Issue / Fail / Critical Fail
- Short note:

---

## Turn 13  (continue the same chat)

### Enter

```text
make 2 of them harder
```

### Expect

- Exactly 2 items become harder; the rest preserved. Still 12, still one correct each.

### Record

- Actual prompt entered:
- Files selected:
- Files Fazah used:
- Result: Pass / Small Issue / Fail / Critical Fail
- Short note:

---

## Turn 14  (continue the same chat)

### Enter

```text
add a multidimensional-array q
```

### Expect

- Adds one multidimensional-array question (arrays of arrays), grounded in php_arrays; count now 13.
- Existing items preserved.

### Record

- Actual prompt entered:
- Files selected:
- Files Fazah used:
- Result: Pass / Small Issue / Fail / Critical Fail
- Short note:

---

## Turn 15  (continue the same chat)

### Enter

```text
add a foreach q too
```

### Expect

- Adds one `foreach` question (`foreach ($arr as $value)` / `as $key => $value`), grounded; count now 14.

### Record

- Actual prompt entered:
- Files selected:
- Files Fazah used:
- Result: Pass / Small Issue / Fail / Critical Fail
- Short note:

---

## Turn 16  (continue the same chat)

### Enter

```text
label the new subtopics
```

### Expect

- The two new items labelled by subtopic (multidimensional / foreach); prior labels intact.

### Record

- Actual prompt entered:
- Files selected:
- Files Fazah used:
- Result: Pass / Small Issue / Fail / Critical Fail
- Short note:

---

## Turn 17  (continue the same chat)

### Enter

```text
re-do the student version, no answers
```

### Expect

- All 14 items as a student version with no correct options or answers shown
  (answer-leakage check — leaked answers = Critical fail).

### Record

- Actual prompt entered:
- Files selected:
- Files Fazah used:
- Result: Pass / Small Issue / Fail / Critical Fail
- Short note:

---

## Turn 18  (continue the same chat)

### Enter

```text
reorder by subtopic again
```

### Expect

- The 14 items regrouped by subtopic; none added or dropped, content unchanged.

### Record

- Actual prompt entered:
- Files selected:
- Files Fazah used:
- Result: Pass / Small Issue / Fail / Critical Fail
- Short note:

---

## Turn 19  (continue the same chat)

### Enter

```text
add explanations for the 2 newest qs to the teacher key
```

### Expect

- The multidimensional and foreach items gain short explanations in the teacher key, grounded in php_arrays.
- Student version stays answer-free.

### Record

- Actual prompt entered:
- Files selected:
- Files Fazah used:
- Result: Pass / Small Issue / Fail / Critical Fail
- Short note:

---

## Turn 20  (continue the same chat)

### Enter

```text
confirm no answers leaked into the student copy
```

### Expect

- Confirms the student version has no answers, marked options, or key
  (answer-leakage check — any leak = Critical fail).

### Record

- Actual prompt entered:
- Files selected:
- Files Fazah used:
- Result: Pass / Small Issue / Fail / Critical Fail
- Short note:

---

## Turn 21  (continue the same chat)

### Enter

```text
final inventory — list all with subtopic
```

### Expect

- Lists all 14 questions (original 12 + multidimensional + foreach) with types and subtopics.
- Counts match the running set.

### Record

- Actual prompt entered:
- Files selected:
- Files Fazah used:
- Result: Pass / Small Issue / Fail / Critical Fail
- Short note:

---

## Turn 22  (continue the same chat)

### Enter

```text
confirm the arrays deck fed all of it
```

### Expect

- Confirms `php_arrays_presentation.pptx` as the single source for every item and both versions.
- Does not claim any other deck (false source claim = Critical fail).

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
