# S028 — PPO vs DPO vs GRPO synthesis across three alignment files

## Tests

With the alignment cheat sheet, the alignment worked problems, and the PA2 deck all selected,
Fazah synthesizes the alignment pipeline across nine turns: PPO's four-model setup, DPO dropping
the reward model, GRPO dropping the critic, and the fact that all three keep a reference model
for KL control — consolidated into a comparison table, a quiz with a checkable numeric item, and
a clean student version.

## Setup

- Start: New chat
- Select files: `09_ar_alignment_rlhf_notes.pdf` + `10_ar_alignment_worked_problems.md` +
  `11_ppo_dpo_grpo_alignment.pptx`
- Do not select: any other course file
- Turns: 9
- Auditor variation: Not allowed

---

## Turn 1

### Enter

```text
walk me through the llm alignment pipeline like i'd present it to the class
```

### Expect

- The PA2 deck's pipeline: start from a pre-trained base language model → human preference data
  as the training signal → reward model trained to score outputs → policy optimization updates
  the LLM, with **KL divergence constraining the policy from drifting**.
- Alignment's goal is stated as making LLMs **helpful, harmless, and honest** (from the deck).
- Grounded in the selected alignment files; no unrelated diffusion/VLM content.

### Record

- Actual prompt entered:
- Files selected:
- Files Fazah used:
- Result: Pass / Small Issue / Fail / Critical Fail
- Short note:

---

## Turn 2   (continue the same chat; keep all three files selected)

### Enter

```text
for ppo, what models do i actually need running at train time
```

### Expect

- Four models, per the PA2 deck: **policy, reference, reward, and critic** — the most complex
  setup among the three methods.
- PPO is framed as RLHF with a separately trained reward model, optimizing the RLHF objective
  with a KL penalty (deck + cheat sheet).
- Bonus grounding (acceptable if mentioned): the clipped surrogate
  L = min(ρ·Â, clip(ρ, 1−ε, 1+ε)·Â) from the notes/worked problems.

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
how does dpo get away with no reward model
```

### Expect

- DPO uses **pairwise preference data directly** — no separate reward model — with a loss derived
  by reparameterizing the RLHF objective (PA2 deck).
- The DPO loss shape matches the notes: −log σ of β times the difference of policy-vs-reference
  log-ratios for the preferred (y+) and rejected (y−) responses.
- The reference model is still present inside the DPO loss (sets up Turn 5); the reward model is
  what disappears, not the reference.

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
and grpo, what does it drop and what replaces it
```

### Expect

- GRPO drops the **critic / value model**; instead it samples a **group of K completions per
  prompt** and normalizes rewards relative to the group (PA2 deck).
- The group-relative advantage matches the notes: Â_i = (r_i − mean of group rewards)/(std of
  group rewards).
- GRPO is not confused with DPO (GRPO still uses rewards; DPO is the one using preference pairs
  without a reward model).

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
do any of the three still need the reference model?
```

### Expect

- Yes — **all three methods keep a reference model for KL control**, exactly as the PA2 deck's
  summary slide states.
- The role is explained consistently: KL against the reference constrains the policy from
  drifting (pipeline slide; PPO's KL-penalized reward; the reference ratios inside the DPO loss).
- No claim that DPO or GRPO eliminates the reference model.

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
make a comparison table of ppo vs dpo vs grpo — models needed, data, complexity
```

### Expect

- One table with the three methods carrying the facts from Turns 2–5: PPO = policy + reference +
  reward + critic (full RLHF pipeline, highest complexity); DPO = preference pairs, no reward
  model; GRPO = group sampling, no critic.
- A row/column reflects that all three keep the reference model for KL.
- Nothing from earlier turns is contradicted; no fourth method or invented property appears.

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
now 5 quiz questions w answers from the table, make one of them a numeric grpo advantage calc
```

### Expect

- Exactly five questions with answers, drawn from the comparison content (which method needs a
  critic, which drops the reward model, what all three keep, etc.).
- The numeric GRPO item is checkable against the worked problems' method — e.g. rewards
  (1, 0, 1, 0) over K=4 give mean 0.5, std 0.5, so the advantage of a reward-1 rollout is +1.0
  (matching `10_ar_alignment_worked_problems.md`).
- All answers stay consistent with the three selected files; nothing invented.

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
student version pls, no answers
```

### Expect

- The same five questions with NO answers shown (answer-leakage check — leaked answers = Critical
  fail).
- The numeric GRPO question keeps its given numbers but not its worked solution.
- Count, order, and topics are unchanged; the teacher version from Turn 7 remains available.

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
which files did u pull from for all of this
```

### Expect

- Fazah names the three selected sources — `09_ar_alignment_rlhf_notes.pdf`,
  `10_ar_alignment_worked_problems.md`, and `11_ppo_dpo_grpo_alignment.pptx` — consistent with
  what it actually used.
- It does not claim any file that was never selected, and does not hedge that it had no source.
- The summary reflects the real artifacts produced (explanations, table, quiz, student version).

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
