# S037 — Quiz quality refinement: numeric verification and student delivery

## Tests

Across eleven turns on one numeric quiz built from the AR/alignment worked-problem set, Fazah
produces questions with numeric answers, has its arithmetic checked against the source's boxed
answers (temperature softmax z=(2,1,0), T=0.5 → p≈(0.867, 0.117, 0.016)), self-reviews and fixes
weak items, and delivers a student copy with no answers while keeping the key in sync.

## Setup

- Start: New chat
- Select files: `10_ar_alignment_worked_problems.md`
- Do not select: `09_ar_alignment_rlhf_notes.pdf`, `11_ppo_dpo_grpo_alignment.pptx`, `13_exam_master_cheatsheet.md`
- Turns: 11
- Auditor variation: Not allowed

---

## Turn 1

### Enter

```text
make a 6 question numeric quiz from this problem set, with full worked answers
```

### Expect

- Exactly six numeric questions, each with a fully worked answer.
- Content is grounded in the worked-problem file (temperature softmax, top-k / top-p, beam search,
  perplexity, PPO clipping, DPO, GRPO advantages).
- Used source = `10_ar_alignment_worked_problems.md`; no citation to an unselected file.

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
make q1 the temperature softmax one, logits (2,1,0) and T=0.5, only change q1
```

### Expect

- Q1 becomes the temperature-softmax question with z=(2,1,0) and T=0.5.
- Its worked answer matches the source: z/T = (4,2,0), sum of exponentials ≈ 62.987,
  p ≈ (0.867, 0.117, 0.016).
- Q2–Q6 are unchanged; still exactly six questions.

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
make one of the others a GRPO advantage q with rewards (1,0,1,0)
```

### Expect

- Exactly one question becomes a GRPO group-advantage question using rewards (1, 0, 1, 0).
- The worked answer matches the source: mean 0.5, population std 0.5, so the advantage of a
  reward-1 rollout is +1.0.
- The remaining questions (including Q1) are unchanged; still six total.

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
double check the arithmetic on every answer, step by step
```

### Expect

- Fazah re-derives each numeric answer step by step and confirms or corrects it.
- Numbers agree with the source's boxed answers where questions mirror it (e.g. top-3 of
  (0.40, 0.25, 0.15) renormalizes to (0.500, 0.3125, 0.1875); perplexity example gives
  L = 1.3246 nats, PPL ≈ 3.76).
- Any error found is fixed in the quiz, not just noted.

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
is q1's answer definitely right? show me the check
```

### Expect

- Fazah verifies Q1 explicitly: e⁴ ≈ 54.598, e² ≈ 7.389, e⁰ = 1, total ≈ 62.987, giving
  p ≈ (0.867, 0.117, 0.016).
- The confirmation matches the source's boxed answer; no silently different numbers.
- Q1's stated answer in the quiz agrees with the check.

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
round all final answers to 3 decimal places, consistently
```

### Expect

- Every final numeric answer is presented to three decimal places (e.g. 0.867 / 0.117 / 0.016).
- Underlying working stays correct; rounding does not change any result materially.
- Questions themselves are not reworded.

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
review ur own quiz, flag anything ambiguous or too easy and fix what u flag
```

### Expect

- A genuine self-review: each question gets a judgement, with specific flags (ambiguous givens,
  missing units/decimals, trivially easy items).
- Flagged items are actually fixed; unflagged items are left alone.
- Fixes stay grounded in the worked-problem file; still six questions.

### Record

- Actual prompt entered:
- Files selected:
- Files Fazah used:
- Result: Pass / Small Issue / Fail / Critical Fail
- Short note:

---

## Turn 8   (continue the same chat)

### Enter

```text
now the student copy, questions only, no answers
```

### Expect

- A student copy with all six questions and NO answers, working, or hints of results
  (answer-leakage check — leaked answers = Critical fail).
- Question wording and numbers match the current teacher version.
- The worked-answer version still exists for the teacher.

### Record

- Actual prompt entered:
- Files selected:
- Files Fazah used:
- Result: Pass / Small Issue / Fail / Critical Fail
- Short note:

---

## Turn 9   (continue the same chat)

### Enter

```text
scan the student copy for any leftover answers or numbers that give it away
```

### Expect

- Fazah checks the actual student copy (not the key) for leaked answers, intermediate values, or
  giveaway phrasing.
- Any leak found is removed (answer-leakage check).
- The confirmation names what was checked, not a generic yes.

### Record

- Actual prompt entered:
- Files selected:
- Files Fazah used:
- Result: Pass / Small Issue / Fail / Critical Fail
- Short note:

---

## Turn 10   (continue the same chat)

### Enter

```text
reorder the student copy easiest to hardest and keep the key in the same order
```

### Expect

- The student copy is reordered easiest → hardest; no question added, dropped, or reworded.
- The teacher key is reordered to match, with each answer still attached to the right question.
- Still six questions in both documents.

### Record

- Actual prompt entered:
- Files selected:
- Files Fazah used:
- Result: Pass / Small Issue / Fail / Critical Fail
- Short note:

---

## Turn 11   (continue the same chat)

### Enter

```text
which file did u use, and confirm the student copy has no answers
```

### Expect

- Fazah names `10_ar_alignment_worked_problems.md` as the single source used throughout.
- It confirms the student copy is answer-free and the teacher version holds the worked answers.
- The summary matches the actual documents (six questions, matching order in copy and key).

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
