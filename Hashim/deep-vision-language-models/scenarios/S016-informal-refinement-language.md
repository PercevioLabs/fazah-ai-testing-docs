# S016 — Informal refinement language

## Tests

Fazah interprets slangy, informal refinement instructions — "spicier", "chill it a bit", "swap q4"
— as precise edits to an alignment quiz, changing only the targeted question each time while the
definitions and the rest of the set stay correct and intact.

## Setup

- Start: New chat
- Select files: none
- Do not select: n/a
- Turns: 7
- Auditor variation: Not allowed

---

## Turn 1

### Enter

```text
need a lil 5 q quiz on rlhf alignment for my class, answers included
```

### Expect

- Produces exactly 5 questions on RLHF/alignment, each with its answer.
- Grounds in the course's alignment material (`09_ar_alignment_rlhf_notes.pdf` and/or
  `11_ppo_dpo_grpo_alignment.pptx`), not generic web content.
- Facts are correct against those sources: reward model trained on preference pairs
  (Bradley–Terry), KL penalty against the reference model, DPO needs no separate reward model.

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
make q2 spicier
```

### Expect

- Reads "spicier" as: make question 2 harder / more interesting — only question 2 changes.
- The other four questions and their answers are untouched; still exactly 5 questions.
- The spicier q2 stays grounded in the alignment sources (no invented methods or properties).

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
nah too hard, chill it a bit
```

### Expect

- Reads the informal walk-back correctly: q2 is eased relative to the turn-2 version (not deleted,
  not reverted into a different topic).
- Only q2 changes; the other four questions remain exactly as before.
- Q2's content stays correct against the alignment sources.

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
swap q4 for something on grpo
```

### Expect

- Question 4 is replaced with a GRPO question; the count stays at exactly 5.
- The GRPO content matches the sources: no critic/value model needed, samples a group of
  completions per prompt, and normalizes rewards relative to the group — advantage
  (r_i − r̄)/σ_r.
- Questions 1–3 and 5 are unchanged (including the chilled q2 from turn 3).

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
q5 feels dry, make it a lil classroom scenario instead
```

### Expect

- Only question 5 is converted into a short scenario-style question; the underlying alignment
  concept it tests is preserved.
- The other four questions are untouched; still exactly 5 questions.
- The scenario's correct answer remains checkable against the alignment sources.

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
kk now gimme all the answers again in one place
```

### Expect

- Produces a consolidated answer key for the CURRENT versions of all 5 questions — including the
  chilled q2, the new GRPO q4, and the scenario q5.
- Answers are correct (e.g. GRPO drops the critic and group-normalizes rewards; DPO drops the
  separate reward model).
- No stale answers from replaced question versions appear.

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
which files did u pull from
```

### Expect

- Names the alignment sources it actually used (`09_ar_alignment_rlhf_notes.pdf` and/or
  `11_ppo_dpo_grpo_alignment.pptx`).
- Does not claim any other or non-existent file.

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
