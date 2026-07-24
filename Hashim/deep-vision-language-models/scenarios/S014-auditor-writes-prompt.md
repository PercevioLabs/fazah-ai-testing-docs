# S014 — Auditor writes the prompt

## Tests

Fazah is robust to realistic, self-composed human wording on the opening turn and then sustains the
same beginner-alignment goal across follow-ups — analogy, PPO/DPO/GRPO comparison, questions,
student version, source — still meeting the underlying goal regardless of the exact phrasing.

## Setup

- Start: New chat
- Select files: `09_ar_alignment_rlhf_notes.pdf`
- Do not select: any other course file
- Turns: 6
- Auditor variation: Allowed — see the Auditor variation section

---

## Turn 1

### Enter

There is no fixed prompt for this scenario. You compose the wording yourself.

Goal: Ask Fazah to explain how RLHF aligns a language model using the selected alignment notes,
for students who have never seen alignment before. Write your own natural prompt in your own
words, then record exactly what you typed.

### Expect

- Explains RLHF grounded in the alignment notes (`09_ar_alignment_rlhf_notes.pdf`): a reward model
  trained on preference pairs (the Bradley–Terry pairwise ranking loss on winning vs losing
  responses), and a policy update whose reward is shaped with a KL penalty against the reference
  model π_ref so the policy does not drift too far.
- Pitched for beginners (plain language, defines terms rather than assuming prior knowledge).
- Content is correct regardless of the exact natural wording you chose.

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
can u add a simple analogy so they can picture what the reward model does
```

### Expect

- Adds one simple analogy for the reward model (scoring/judging outputs) without changing the
  explanation from turn 1.
- Analogy is beginner-appropriate and does not misrepresent the pipeline (the reward model scores
  responses; it is trained from pairwise preferences).

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
ok now compare ppo, dpo and grpo plainly, whats different about each
```

### Expect

- Comparison matches the notes: **PPO** uses the clipped surrogate objective with an advantage and
  KL-penalized reward against π_ref; **DPO** bypasses the separate reward model and directly widens
  the probability gap between preferred and rejected responses relative to the reference model;
  **GRPO** computes advantage without a value model by sampling a group of completions and
  normalizing rewards as (r_i − r̄)/σ_r.
- Plain, beginner-level wording consistent with turns 1–2.
- No method is attributed a property it does not have (e.g. DPO does not need a separate reward
  model).

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
make 4 beginner qs on this
```

### Expect

- Produces exactly four beginner-level questions about the alignment material (reward model, KL
  penalty, PPO vs DPO vs GRPO differences).
- Questions match the beginner audience and draw only on what was covered above.

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
now gimme a student version of those questions
```

### Expect

- Produces the four questions with NO answers shown (student version).
- Answer leakage into the student version = Critical fail.
- Same four questions as turn 4.

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
confirm which file u used
```

### Expect

- Names the alignment notes (`09_ar_alignment_rlhf_notes.pdf`) as the source.
- Does not claim any other or non-existent file.

### Record

- Actual prompt entered:
- Files selected:
- Files Fazah used:
- Result: Pass / Small Issue / Fail / Critical Fail
- Short note:

---

## Auditor variation

Add or change one realistic instruction. Record exactly what you entered. Do not change the
scenario's main goal.

Example variations:

- Change the student audience on Turn 1 (e.g. "for final-year undergrads" instead of MS students).
- Add "keep it under one minute to read" to Turn 1.
- Ask for the Turn 2 analogy in a specific domain (e.g. sports or cooking).
- Use a more formal tone throughout.

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
