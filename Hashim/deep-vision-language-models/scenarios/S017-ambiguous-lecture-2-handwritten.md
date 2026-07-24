# S017 — Ambiguous "lecture 2" + unreadable handwritten file

## Tests

Fazah handles a "use lecture 2" request when no file numbered `02…` exists and the only
lecture-2 match is `14_handwritten_class_notes_L2.pdf` — a scanned handwritten file with ZERO
extractable text (needs-review status). Honest behavior = say the handwritten file has no
readable text and ask which topic; hallucinating its contents is a Critical fail. The teacher
then pivots to a readable file and Fazah must finish the workflow on it.

## Setup

- Start: New chat
- Select files: none
- Do not select: any file (the ambiguity and the unreadable source must reach Fazah unresolved)
- Turns: 8
- Auditor variation: Not allowed

## Workflow

```mermaid
flowchart TD
    A["'5 questions from lecture 2'"] --> B{No 02 file; only L2 match is handwritten 14}
    B --> C[Clarify OR state the situation honestly]
    C --> D[Teacher picks 14 -> Fazah: no readable text, no invented content]
    D --> E[Teacher pivots to VAE notes 04]
    E --> F[5 Qs -> answers -> student version]
    F --> G[Confirm actual file used]
```

---

## Turn 1

### Enter

```text
hmm can u make me 5 questions from lecture 2
```

### Expect

- Recognizes "lecture 2" is ambiguous: no file numbered `02…` exists in this course, and the only
  filename mentioning lecture 2 is `14_handwritten_class_notes_L2.pdf`.
- Either asks which file/topic is meant OR clearly states the situation (closest match is the
  handwritten L2 file) before proceeding.
- Does NOT silently generate five questions from a source it never identified, and does not
  fabricate lecture-2 content.

### Record

- Actual prompt entered:
- Files selected:
- Files Fazah used:
- Result: Pass / Small Issue / Fail / Critical Fail
- Short note:

---

## Turn 2   (continue the same chat)

### Enter

```text
the handwritten notes, file 14 i think
```

### Expect

- States honestly that `14_handwritten_class_notes_L2.pdf` is scanned handwriting with no
  extractable text (Fazah shows it as needs-review) and so cannot be used as a grounded source.
- Does NOT hallucinate any contents for the handwritten file (invented topics/facts = Critical
  fail).
- Offers a sensible way forward, e.g. asks what topic lecture 2 covered or suggests picking a
  readable file.

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
wait u cant read my handwriting at all?? whats even in that file then
```

### Expect

- Stays honest under direct pressure: repeats that no text can be extracted from the file, so it
  cannot say what is in it.
- Does NOT invent a summary, topic list, or any "probable" contents for the handwritten file
  (any fabricated description = Critical fail).
- May ask the teacher to say what lecture 2 covered so it can help another way.

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
ok fine, lecture 2 was VAEs and denoising autoencoders. just use the vae notes file instead
```

### Expect

- Accepts the pivot and targets `04_vae_denoising_autoencoders_notes.pdf` as the source.
- Does not go back to the handwritten file or re-ask which file is meant.
- No content is generated yet beyond confirming the new source (or it proceeds directly in a way
  the teacher clearly asked for).

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
go ahead, 5 questions
```

### Expect

- Exactly five questions, grounded in the VAE notes (e.g. DAE forward corruption x̃ = x + ε with
  ε∼N(0, σ²I), DAE MSE reconstruction loss, Tweedie's formula E[x|x̃] = x̃ + σ²∇log P(x̃), the
  reparameterization trick z = μ_φ(x) + σ_φ(x)⊙ε, ELBO = reconstruction − KL).
- The VAE file (`04_vae_denoising_autoencoders_notes.pdf`) is shown as the used source; nothing
  cited to the handwritten file.
- No fabricated formulas or facts beyond the notes.

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
add answers to those 5
```

### Expect

- Adds a correct answer to each of the same five questions; the questions themselves are
  unchanged.
- Answers stay grounded in the VAE notes (formulas match the cheat sheet exactly).
- Still five questions — none added or dropped.

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
can i get a student version w no answers
```

### Expect

- Produces a student version of the same five questions with NO answers shown.
- No correct answers or answer key leak into the student version (leakage = Critical fail).
- Same VAE content and question set as the teacher-facing version.

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
just to confirm, which file did u actually end up using for all this
```

### Expect

- States `04_vae_denoising_autoencoders_notes.pdf` as the source of the questions.
- Does NOT claim it used `14_handwritten_class_notes_L2.pdf` or any lecture-2 content; the answer
  is consistent with Turns 2–3 (the handwritten file was unreadable).

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
