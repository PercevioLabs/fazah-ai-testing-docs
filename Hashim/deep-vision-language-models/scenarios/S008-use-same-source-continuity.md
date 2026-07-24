# S008 — "Use the same source" continuity across artifact types

## Tests

With only the VLM notes selected, Fazah carries one source through a long chain of different
artifact types — explanation, quiz, student version, student notes, a trim, and a topic summary —
honoring repeated "same source" instructions and never drifting to other course material.

## Setup

- Start: New chat
- Select files: `12_vlm_vit_clip_reasoning.md`
- Do not select: any other course file
- Turns: 9
- Auditor variation: Not allowed

---

## Turn 1

### Enter

```text
explain how a vit turns an image into tokens
```

### Expect

- Patch tokenization per the notes: N = (H/P)·(W/P) spatial patches; for 224×224 with P=16 that is
  14×14 = 196 patches, and with the prepended [CLS] token the sequence length is L = N+1 = 197.
- Patch-embedding layer as a linear projection of the flattened patch, params (P·P·C)·D + D — for
  D=768 the notes' worked value is 590,592 (if a number is given, it must match).
- Grounded in the selected VLM notes (`12_vlm_vit_clip_reasoning.md`), not a generic web answer.

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
now the clip loss from the same notes
```

### Expect

- Temperature-scaled logits ℓ_ij = u_iᵀv_j/τ on L2-normalized embeddings; per-image
  L_{I→T} = −log(exp(ℓ_ii)/Σ_j exp(ℓ_ij)); full symmetric loss L = ½(L_{I→T} + L_{T→I}) — matching
  the notes.
- Lower τ sharpens the softmax (per the notes' Problem 3) if temperature is discussed.
- Still grounded in `12_vlm_vit_clip_reasoning.md`.

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
last bit — cross attention, what are the shapes
```

### Expect

- Attn(Q, K, V) = softmax(QKᵀ/√d)·V with Q ∈ R^{Lq×d}, K, V ∈ R^{Lk×d}, output ∈ R^{Lq×d} —
  matching the notes.
- The text-query-to-image-keys framing is consistent with the notes' cross-attention problem; no
  shapes are invented.
- Same source as before.

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
make a 6 question quiz on those three topics, same source, with answers
```

### Expect

- Exactly six questions spread across the three topics built above (patch tokenization, CLIP loss,
  cross-attention), each answer supported by the VLM notes (e.g. 196/197; ½(L_{I→T}+L_{T→I});
  output shape R^{Lq×d}).
- No question drifts to unselected material (diffusion, alignment, etc.).
- Used sources still reflect only `12_vlm_vit_clip_reasoning.md`.

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
student version, no answers
```

### Expect

- The same six questions in a student-facing version with NO answers shown
  (answer-leakage check — leaked answers = Critical fail).
- The teacher version from Turn 4 is preserved as its own version.

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
now student notes covering the same three topics, use the same source
```

### Expect

- A new artifact type (student-facing notes) covering patch tokenization, CLIP loss, and
  cross-attention, still exclusively from the VLM notes.
- Content stays consistent with what was established in Turns 1–3 (same formulas, same numbers).
- The quiz versions from Turns 4–5 are preserved, not overwritten.

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
trim those notes to about half, keep all three topics
```

### Expect

- The student notes are condensed to roughly half while all three topic sections survive.
- Surviving formulas and numbers remain correct (e.g. 197 tokens, ½(L_{I→T}+L_{T→I})); nothing new
  is introduced from outside the source.
- Only the notes change; the quizzes are untouched.

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
and a short topic summary for my lesson plan, same source again
```

### Expect

- A third artifact type: a brief teacher-facing topic summary of the three VLM topics, again from
  `12_vlm_vit_clip_reasoning.md` only.
- Consistent with everything built so far; no drift to other course files after eight turns.

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
list everything we made and confirm it all came from one file
```

### Expect

- An inventory of the artifacts actually produced (explanations, teacher quiz, student quiz,
  student notes, trimmed notes, topic summary) — no fabricated extras.
- Fazah confirms the single source `12_vlm_vit_clip_reasoning.md` for all of it; it does not claim
  any file that was never selected.

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
