# S002 — No selected file, clear flow-matching topic

## Tests

With no file selected but a clearly flow-matching question, Fazah auto-selects the flow-matching
notes as the source, then stays on that same source across a sustained workflow — SDE framing,
predictor-corrector, and a quiz with teacher and student versions.

## Setup

- Start: New chat
- Select files: none
- Do not select: anything (the point is that Fazah must find `07_flow_matching_notes.pdf` itself)
- Turns: 6
- Auditor variation: Not allowed

---

## Turn 1

### Enter

```text
explain the flow matching linear interpolant to me, whats the network trained to predict
```

### Expect

- Fazah auto-selects / grounds on the flow-matching notes (`07_flow_matching_notes.pdf`) without
  being told; used sources reflect that file, not a generic web answer.
- Linear interpolant: x_t = t·x_1 + (1−t)·x_0, where t=0 is pure noise (x_0) and t=1 is clean data
  (x_1) — matching the notes.
- The network's target is the standard flow target velocity v = x_1 − x_0, a constant vector along
  the straight-line trajectory.

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
how does that file frame the ve and vp sdes, whats the drift for each
```

### Expect

- VE-SDE (the NCSN case) has **zero drift, f = 0**; VP-SDE (the DDPM case) has drift
  **f = −½β(t)·x_t** — matching the notes' drift/diffusion identification.
- f(x,t) is identified as the drift coefficient (the dt multiplier) and g(t) as the diffusion
  coefficient (the dW multiplier).
- Still grounded in `07_flow_matching_notes.pdf`; the source does not silently change.

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
and the predictor-corrector sampler, whats each half doing
```

### Expect

- Predictor = the Euler–Maruyama discretization of the reverse SDE (finite step Δt, plus a
  √Δt-scaled fresh noise vector Z_i); corrector = Langevin steps — matching the notes' Part 2.
- The deterministic alternative is the probability-flow ODE, where the score term is **halved**
  (the ½g² multiplier) and the random Z noise term is **dropped entirely** — the notes' trap
  warning.
- No sampler mechanics are invented beyond what the flow-matching notes contain.

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
nice, make a 5 question quiz on all of that w/ answers
```

### Expect

- Exactly five questions covering the material built up above (interpolant, target velocity, VE/VP
  drift, predictor-corrector, ODE-vs-SDE), not new topics.
- Each answer is supported by the flow-matching notes (e.g. v = x_1 − x_0; VE drift = 0; ODE step
  halves the score term and drops the noise).
- Still grounded in `07_flow_matching_notes.pdf`.

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
student version of the quiz pls, no answers
```

### Expect

- The same five questions in a student-facing version with NO answers shown
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
i never picked a file — which one did you end up using
```

### Expect

- Fazah names the flow-matching notes (`07_flow_matching_notes.pdf`) as the source it selected and
  used throughout.
- It does not claim the teacher selected it, does not invent additional sources, and does not hedge
  that it had no source.

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
