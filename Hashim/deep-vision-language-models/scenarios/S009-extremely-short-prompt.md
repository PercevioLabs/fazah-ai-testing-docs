# S009 — Extremely short prompt

## Tests

Fazah recognizes the intended concept from a minimal one-word prompt and sustains a terse, rushed
teacher's follow-ups on the same DDIM/DDPM topic — including building and hardening a quiz — without
over-clarifying or losing context.

## Setup

- Start: New chat
- Select files: none
- Do not select: n/a
- Turns: 6
- Auditor variation: Not allowed

---

## Turn 1

### Enter

```text
ddim?
```

### Expect

- Recognizes the intent as the DDIM sampler from the diffusion notes
  (`06_diffusion_ddpm_ddim_notes.pdf`) — not something unrelated.
- Describes DDIM as the non-Markovian sampler that forms the intermediate clean prediction x̂_0 and
  can jump/skip steps from t to t′ — matching the notes.
- Proceeds rather than over-clarifying a clear (if terse) request.

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
eta?
```

### Expect

- Resolves the terse follow-up from context: η is the DDIM stochasticity parameter inside the
  variance σ_t (how much randomness is injected).
- States that **η = 0 makes σ_t = 0 and sampling deterministic** (the notes' "ODE solver /
  deterministic generation / perfectly reversible" case).
- States that η = 1 blends toward DDPM behavior — consistent with the notes' DDIM-to-DDPM
  connection.

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
vs ddpm
```

### Expect

- Contrasts the two samplers as in the notes: DDPM is the standard Markovian step — exactly one
  step backward at a time with fresh σ_t·z noise each step; DDIM is non-Markovian and can skip
  steps, and is deterministic at η = 0.
- Notes the collapse case: with t′ = t−1 (no skipping) and η = 1, the DDIM formula collapses into
  the standard DDPM step.
- Stays on the same DDIM/DDPM thread from turns 1–2 (does not restart or switch topic).

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
quiz
```

### Expect

- Produces a short quiz on the DDIM/DDPM/η material built up above — not new topics like flow
  matching or score networks.
- Questions are answerable from the diffusion notes (e.g. η=0 → deterministic; DDPM one step at a
  time vs DDIM step-skipping).
- Does not stall on the one-word prompt with unnecessary clarification.

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
harder
```

### Expect

- Produces a harder version of the same quiz — same number of questions, same DDIM/DDPM topic.
- Increased difficulty stays grounded in the notes (e.g. the η/σ_t variance expression, the
  DDIM-to-DDPM collapse conditions) rather than inventing content outside them.
- The previous quiz is treated as the thing being revised, not forgotten.

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
answers?
```

### Expect

- Provides an answer key for the current (harder) quiz — one answer per question, matched to the
  right questions.
- Answers are correct against the notes: η=0 ⇒ σ_t = 0 ⇒ deterministic; η=1 with t′=t−1 recovers
  DDPM; DDPM injects fresh noise each step.
- Does not change the questions while answering them.

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
