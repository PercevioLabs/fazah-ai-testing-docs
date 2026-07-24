# S012 — Large instruction-heavy lesson request

## Tests

Fazah satisfies one long, constraint-dense lesson-plan prompt on flow matching — timing, ordering,
a derivation, exactly two worked examples, an exit ticket, and a no-code rule — and then survives a
run of targeted refinements without breaking the earlier constraints.

## Setup

- Start: New chat
- Select files: `07_flow_matching_notes.pdf`
- Do not select: any other course file
- Turns: 8
- Auditor variation: Not allowed

---

## Turn 1

### Enter

```text
plan me a 90 min lesson on flow matching from the selected notes. rules:
- open with a 15 min recap of the SDE view, VE vs VP, drift and diffusion coefficients
- then derive the linear interpolant x_t = (1-t)x0 + t x1 step by step
- include exactly 2 worked examples with actual numbers
- end with a 5 question exit ticket
- no code anywhere, this is a theory session
- give timing for every section and it has to add up to 90
```

### Expect

- All constraints honored in one pass: 90-minute plan, SDE recap first (15 min), interpolant
  derivation, exactly 2 numeric worked examples, a 5-question exit ticket, zero code, and section
  timings that sum to 90.
- SDE recap matches the notes: VE-SDE (NCSN) has zero drift (f = 0); VP-SDE (DDPM) has drift
  f = −½β(t)x_t; g(t) is the diffusion coefficient on dW_t.
- Interpolant section matches the notes: x_t = (1−t)x_0 + t·x_1 with t=0 pure noise, t=1 clean
  data, and target velocity v = x_1 − x_0.
- Content is grounded in `07_flow_matching_notes.pdf`, not generic web material.

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
the sde recap is too heavy, cut it to 10 min and give those 5 min to the interpolant part
```

### Expect

- The recap becomes 10 minutes and the interpolant section gains exactly 5 minutes; total still
  sums to 90.
- No sections are dropped; the two worked examples, exit ticket, and no-code rule survive.
- Recap content stays correct (VE f=0 vs VP f=−½β(t)x_t) after trimming.

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
swap worked example 2 for one on the target velocity
```

### Expect

- Only example 2 is replaced; example 1 is unchanged; still exactly 2 worked examples.
- The new example computes the target velocity as v = x_1 − x_0 for a concrete noise/data pair —
  matching the notes' standard flow target velocity.
- The arithmetic in the new example is correct.

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
add a 2 min note on the probability flow ODE at the end of the recap
```

### Expect

- A short ODE note is added inside the recap, matching the notes: the probability-flow ODE is the
  deterministic equation sharing the SDE's marginals, with the critical ½ multiplier on the
  g²(t)·score term and NO random noise term.
- Timing is rebalanced so the total still sums to 90.
- Nothing else in the plan is rewritten.

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
make the exit ticket harder but keep it at 5 questions
```

### Expect

- Exit ticket still has exactly 5 questions, now harder.
- Harder questions stay inside the notes' content (VE/VP drift identification, Euler–Maruyama
  predictor step, interpolant position, target velocity, ODE vs SDE step differences).
- The rest of the lesson plan is untouched.

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
now give me the exit ticket answer key separately
```

### Expect

- A separate answer key covering all 5 current questions, matched to the right questions.
- Answers are correct against the notes (e.g. v = x_1 − x_0; VE drift is zero; the ODE step halves
  the score term and drops the Z noise term).
- The exit ticket itself is not modified while the key is produced.

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
condense the whole plan into a one page handout for my TA
```

### Expect

- A condensed one-page version preserving the structure: 10-min recap (with the ODE note), the
  interpolant derivation, both worked examples, exit ticket, timings summing to 90.
- No code appears (the turn-1 rule persists); no formulas are altered in the compression.
- The full plan from earlier turns is not lost or contradicted.

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
confirm u only used the flow matching notes for this
```

### Expect

- Names the flow-matching notes (`07_flow_matching_notes.pdf`) as the source used throughout.
- Does not claim any file that was never selected, and does not hedge that it had no source.

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
