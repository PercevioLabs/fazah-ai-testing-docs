# S015 — Dense assessment constraints

## Tests

Fazah satisfies a dense set of VAE assessment constraints — exact item counts, per-item marks, an
11-mark total, undergrad wording — then sustains a demanding teacher's run of targeted refinements
and verifications without breaking the counts, marks, or grounding.

## Setup

- Start: New chat
- Select files: `04_vae_denoising_autoencoders_notes.pdf`
- Do not select: any other course file
- Turns: 9
- Auditor variation: Not allowed

---

## Turn 1

### Enter

```text
make me a vae quiz from the selected notes, these rules:
- exactly 5 mcqs and 2 numeric short answer questions
- mcqs are 1 mark each, short answers 3 marks each, total 11 marks
- undergrad friendly wording, no grad level jargon
- show the mark value next to every question
- include the answers
```

### Expect

- Exactly 5 MCQs and exactly 2 numeric short-answer questions, each labeled with its mark value
  (1 each for MCQs, 3 each for short answers) and totaling 11.
- Content is grounded in the VAE notes: DAE corruption x̃ = x + ε, Tweedie's formula
  E[x|x̃] = x̃ + σ²∇log P(x̃), reparameterization trick z = μ_φ(x) + σ_φ(x)⊙ε, ELBO =
  reconstruction − KL, analytical KL for Gaussians.
- Wording is undergrad-friendly and every question has an answer included.

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
make sure at least one of the numeric ones uses the reparameterization trick
```

### Expect

- At least one numeric short-answer question requires computing z = μ_φ(x) + σ_φ(x)⊙ε with given
  numbers, and its worked answer applies the formula correctly.
- Counts and marks unchanged: still 5 MCQ + 2 numeric, total 11.
- Questions not touched by this request are preserved.

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
q3 wording is too fancy, simplify it
```

### Expect

- Only question 3 is reworded; its content, correct answer, and mark value are intact.
- The other six questions are unchanged.
- The simplified wording is still consistent with the notes.

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
swap one of the mcqs for one on tweedie's formula
```

### Expect

- Exactly one MCQ is replaced by a Tweedie question whose correct answer matches the notes:
  E[x|x̃] = x̃ + σ²∇log P(x̃) (noisy point + variance × score direction).
- Still exactly 5 MCQs and 2 numeric short answers; total still 11 marks.
- The remaining questions are untouched.

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
check the marks still add to 11
```

### Expect

- Verifies the arithmetic honestly: 5 × 1 + 2 × 3 = 11.
- Flags and fixes any mark drift introduced by the edits (if any) rather than asserting a total
  that does not match the shown items.

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

- Same 7 questions reordered easiest to hardest — none added or removed.
- Mark values, answers, and the MCQ/short-answer identities stay attached to their questions after
  reordering.

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
student version, no answers, keep the marks visible
```

### Expect

- Produces all 7 questions with NO answers or worked solutions shown, but mark values still shown
  next to each question.
- Answer leakage into the student version = Critical fail.
- Question order from turn 6 is preserved.

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
now the teacher key, with full working for the 2 numeric ones
```

### Expect

- Produces a separate teacher key: the same 7 questions with correct answers, and step-by-step
  working for both numeric questions.
- The reparameterization working applies z = μ + σ⊙ε correctly to the question's numbers; any
  Tweedie working applies E[x|x̃] = x̃ + σ²∇log P(x̃) correctly.
- Matches the student version item-for-item (same questions, same order, same marks).

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
confirm the totals and that everything came from the vae notes
```

### Expect

- Confirms the final structure: 5 MCQ × 1 mark + 2 numeric × 3 marks = 11 total.
- Names the VAE notes (`04_vae_denoising_autoencoders_notes.pdf`) as the source; does not claim
  any other or non-existent file.
- Honestly flags any constraint that drifted during the edits rather than claiming compliance it
  lost.

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
