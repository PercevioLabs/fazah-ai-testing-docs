# S026 — DDPM vs DDIM sampling and the η parameter, then question generation

## Tests

With only the diffusion cheat sheet selected, Fazah keeps DDPM and DDIM sampling correctly
distinguished across the conversation — stochastic Markovian steps vs the x̂_0-based jump, η=0
deterministic vs η=1 collapsing back to DDPM — then generates questions from the thread, applies
a targeted edit, and delivers a clean student copy naming its source.

## Setup

- Start: New chat
- Select files: `06_diffusion_ddpm_ddim_notes.pdf`
- Do not select: `05_ncsn_score_based_models_notes.pdf`, `07_flow_matching_notes.pdf`,
  `08_diffusion_score_flow_worked_problems.md`
- Turns: 6
- Auditor variation: Not allowed

---

## Turn 1

### Enter

```text
my students mix up ddpm and ddim sampling, give me a clean explanation of the difference
```

### Expect

- DDPM = the standard Markovian denoising step: exactly one step backward at a time, with a fresh
  stochastic injection σ_t·z each step; DDIM = non-Markovian step-skipping that first forms the
  intermediate clean prediction x̂_0 = (1/√ᾱ_t)(x_t − √(1−ᾱ_t)·ε_θ) and then jumps from t to t′.
- The stochastic-vs-can-be-deterministic contrast is stated correctly (DDPM injects noise every
  step; DDIM's randomness is controlled by its variance term).
- Grounded in the selected diffusion notes, not a generic web answer; no unselected file is cited.

### Record

- Actual prompt entered:
- Files selected:
- Files Fazah used:
- Result: Pass / Small Issue / Fail / Critical Fail
- Short note:

---

## Turn 2   (continue the same chat; keep `06_diffusion_ddpm_ddim_notes.pdf` selected)

### Enter

```text
where does eta come into this, what do the extreme values do
```

### Expect

- η is the stochasticity parameter in the DDIM variance σ_t: **η = 0 makes σ_t = 0**, the z noise
  term disappears, and sampling is deterministic (the notes' "ODE solver / deterministic
  generation / perfectly reversible" case).
- **η = 1 with t′ = t−1** (no skipping) collapses the DDIM formula back into the standard DDPM
  step — the notes' "DDIM to DDPM connection".
- The Turn 1 distinction is extended, not rewritten or contradicted; still grounded in the
  diffusion notes.

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
so if i want the exact same image every run, what do i set and why does that work
```

### Expect

- Set η = 0: then σ_t = 0, the z term vanishes, and generation is deterministic / perfectly
  reversible — matching the notes' deterministic-DDIM caveat.
- The "why" traces through the DDIM variance formula (η scales σ_t, so η=0 removes all injected
  randomness), consistent with Turn 2.
- No invented claim (e.g. that DDPM can be made deterministic the same way mid-trajectory) beyond
  what the notes support.

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
make 4 short questions w answers from what we covered
```

### Expect

- Exactly four questions, drawn from the DDPM/DDIM/η material built up in Turns 1–3 (not new
  topics like score networks or flow matching).
- Each answer is supported by the diffusion notes (e.g. DDPM one-step + fresh noise; x̂_0 jump;
  η=0 deterministic; η=1 & t′=t−1 → DDPM).
- Still grounded in `06_diffusion_ddpm_ddim_notes.pdf`.

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
change q4 only — make it ask what happens at eta 0 vs eta 1
```

### Expect

- Only question 4 changes; questions 1–3 are untouched.
- The new q4 answer matches the notes: η=0 → σ_t=0, deterministic/reversible; η=1 with t′=t−1 →
  collapses to the standard DDPM step.
- Still exactly four questions; the revision updates the existing set rather than regenerating it.

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
gimme a student copy w no answers, and tell me which file all this came from
```

### Expect

- The same four questions in a student copy with NO answers (answers leaking = Critical fail).
- Fazah names `06_diffusion_ddpm_ddim_notes.pdf` as the source used throughout, and claims no
  file that was never selected.
- Question count and the Turn 5 edit are preserved in the student copy.

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
