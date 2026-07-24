# S007 — Explicit selection overrides source history

## Tests

After several turns of alignment work grounded in the RLHF notes, the teacher explicitly selects
the VLM notes and pivots topics. Fazah must let the current explicit selection win over the recent
conversational context — answering ViT/CLIP questions from the VLM notes only, and keeping the new
quiz free of alignment material.

## Setup

- Start: New chat
- Select files: `09_ar_alignment_rlhf_notes.pdf` (switched to `12_vlm_vit_clip_reasoning.md`
  before Turn 4)
- Do not select: any other course file
- Turns: 7
- Auditor variation: Not allowed

---

## Turn 1  (alignment notes selected)

### Enter

```text
whats the kl penalty doing in the ppo reward shaping
```

### Expect

- The per-token shaped reward subtracts β·log(π_θ(y_t|s)/π_ref(y_t|s)) — penalizing the policy for
  deviating too far from the base reference model — matching the notes.
- Grounded in the selected alignment notes (`09_ar_alignment_rlhf_notes.pdf`), not a generic web
  answer.
- No invented citation to a file that was not selected.

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
and the bradley-terry reward model loss
```

### Expect

- L(ψ) = −log σ(r_ψ(x, y+) − r_ψ(x, y−)) — trains the reward model to score the winning response
  above the losing one — matching the notes' "Reward Model (Critic) Loss".
- Still grounded in `09_ar_alignment_rlhf_notes.pdf`.

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
quick 3 question quiz on that w/ answers
```

### Expect

- Exactly three questions on the KL penalty / Bradley–Terry material built above, with answers
  supported by the alignment notes.
- Still grounded in the alignment notes.

### Record

- Actual prompt entered:
- Files selected:
- Files Fazah used:
- Result: Pass / Small Issue / Fail / Critical Fail
- Short note:

---

## Turn 4  (before entering: deselect the alignment notes, select `12_vlm_vit_clip_reasoning.md`; continue the same chat)

### Enter

```text
ok switching gears, use the vlm notes now. how many tokens does a vit get from a 224x224 image with patch size 16
```

### Expect

- Fazah answers from the newly selected VLM notes: 224/16 = 14 patches per side, N = 14×14 =
  **196 spatial patches**, and with the prepended [CLS] token L = **197 tokens** — matching the
  notes' Problem 1.
- Used sources now reflect `12_vlm_vit_clip_reasoning.md`; the current explicit selection wins
  over the recent alignment context (continuing to answer from the alignment notes = Fail).
- No alignment content bleeds into the answer.

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
and hows the clip contrastive loss set up
```

### Expect

- CLIP's symmetric contrastive (InfoNCE) loss over temperature-scaled logits ℓ_ij = u_iᵀv_j/τ:
  per image, L_{I→T} = −log(exp(ℓ_ii)/Σ_j exp(ℓ_ij)), full loss L = ½(L_{I→T} + L_{T→I}) — matching
  the VLM notes.
- Lower τ magnifies the logits and sharpens the softmax (per the notes' Problem 3), if temperature
  behavior is discussed.
- Grounded in `12_vlm_vit_clip_reasoning.md` only.

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
make a 4 question quiz on the vlm stuff, dont mix in the alignment material from earlier
```

### Expect

- Exactly four questions, all from the VLM notes (patch/token counts, CLIP loss/temperature,
  cross-attention shapes, etc.), each with an answer supported by
  `12_vlm_vit_clip_reasoning.md`.
- ZERO questions on PPO/KL/Bradley–Terry — leaking the earlier alignment material into this quiz =
  Fail on missed instruction.
- Used sources reflect only the VLM notes.

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
which file did that last quiz come from
```

### Expect

- Fazah names the VLM notes (`12_vlm_vit_clip_reasoning.md`) as the source of the Turn 6 quiz.
- It does not credit the alignment notes for the VLM quiz, and does not claim any file that was
  never selected.

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
