# S024 — GET vs POST, compare then assess (auditor variation)

## Tests

With only the forms deck selected, Fazah compares GET and POST on the terms the deck uses, then holds
a conversational build — a realistic case for each, a forgettable difference, a table, a limitation,
teacher and student questions, and the validate/sanitize security note — all grounded in `php_forms`
without inventing behaviour the deck does not state.

## Setup

- Start: New chat
- Select files: `php_forms_presentation.pptx`
- Do not select: any other deck
- Turns: 14
- Auditor variation: Allowed (see the Auditor variation section)

---

## Turn 1

### Enter

```text
ok so can u compare GET and POST
```

### Expect

- GET = visible in the URL, bookmarkable/cached/in history, ~2000-char limit, not for sensitive data,
  no file uploads; POST = not in the URL, no size limit, file uploads, secure for passwords — per the deck.
- Notes POST is the recommended method for forms.
- Grounded in the selected forms deck (grounding badge / php_forms under used sources), not a generic answer.

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
gimme one realistic case where each fits
```

### Expect

- One fitting case for GET (bookmarkable/shareable, e.g. a search query in the URL) and one for POST
  (sensitive or large data, e.g. a login/password or a file upload) — framed as the deck frames them.
- No behaviour beyond the deck (no headers, cookies, REST detail, etc.).
- Still grounded in `php_forms`.

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
whats one key difference i might forget
```

### Expect

- Adds a real deck detail that is easy to miss: GET's ~2000-char limit / no file uploads, or that GET
  data is visible in the URL and cached in history, or that POST is the recommended form method.
- Keeps the earlier comparison; extends rather than rewrites.
- Still grounded in `php_forms`.

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
cool put that in a table
```

### Expect

- A table contrasting GET vs POST on the points built up (URL visibility, size limit, file uploads,
  bookmarkable/cached, sensitive data, recommended for forms).
- No new claims added; only reformatted.
- Still grounded in `php_forms`.

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
ok now add a limitation of each
```

### Expect

- A limitation for GET (size cap, unsafe for sensitive data, no file uploads) and one for POST
  (not bookmarkable/cached) — all from the deck.
- Extends the comparison; nothing earlier is dropped or contradicted.
- Still grounded in `php_forms`.

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
make 4 qs from this
```

### Expect

- Exactly 4 questions on GET vs POST, drawn from the material above, not new topics.
- Any answers given are consistent with the deck (POST recommended for forms; GET visible in URL; no
  uploads on GET; POST for passwords).
- Still grounded in `php_forms`.

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
now a student version no answers
```

### Expect

- The same 4 questions, student-facing, with NO answers shown
  (answer-leakage check — leaked answers = Critical fail).
- The teacher version from Turn 6 is preserved; only the student copy is produced.

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
which deck is this from btw
```

### Expect

- Names the forms deck (`php_forms_presentation.pptx`) as the source used throughout.
- Does not claim a deck that was never selected, and does not hedge that it had no source.

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
add the security note about validating and sanitizing
```

### Expect

- Adds the deck's security point: never trust user input; always validate and sanitize form data.
- Extends the material without disturbing the comparison or the quiz.
- Still grounded in `php_forms`.

### Record

- Actual prompt entered:
- Files selected:
- Files Fazah used:
- Result: Pass / Small Issue / Fail / Critical Fail
- Short note:

---

## Turn 10  (continue the same chat)

### Enter

```text
ok make them harder
```

### Expect

- The 4 questions become harder while staying on GET vs POST; still exactly 4, still answerable from
  the deck.
- Any current student (no-answers) copy is not made to leak answers.
- Still grounded in `php_forms`.

### Record

- Actual prompt entered:
- Files selected:
- Files Fazah used:
- Result: Pass / Small Issue / Fail / Critical Fail
- Short note:

---

## Turn 11  (continue the same chat)

### Enter

```text
and a teacher key
```

### Expect

- A teacher key with the correct answer + a short explanation for each of the 4 questions.
- Answers follow the deck; the student version stays answer-free.
- Still grounded in `php_forms`.

### Record

- Actual prompt entered:
- Files selected:
- Files Fazah used:
- Result: Pass / Small Issue / Fail / Critical Fail
- Short note:

---

## Turn 12  (continue the same chat)

### Enter

```text
add a scenario q
```

### Expect

- Adds one scenario-framed question (e.g. which method for a login form and why → POST; hidden from
  URL, no size limit, secure).
- The correct answer follows the deck; the existing 4 questions are kept.
- Still grounded in `php_forms`.

### Record

- Actual prompt entered:
- Files selected:
- Files Fazah used:
- Result: Pass / Small Issue / Fail / Critical Fail
- Short note:

---

## Turn 13  (continue the same chat)

### Enter

```text
reorder them easiest to hardest
```

### Expect

- The same questions (4 base + the scenario item) reordered easiest → hardest; content unchanged,
  none added or dropped.
- Still grounded in `php_forms`.

### Record

- Actual prompt entered:
- Files selected:
- Files Fazah used:
- Result: Pass / Small Issue / Fail / Critical Fail
- Short note:

---

## Turn 14  (continue the same chat)

### Enter

```text
can u double check nothing broke
```

### Expect

- Confirms the current state: GET vs POST comparison + table + limitation + security note, and the
  quiz (teacher version, student version, teacher key, scenario item) with an accurate count.
- No silent additions, drops, or contradictions.
- Still attributes everything to `php_forms` only.

### Record

- Actual prompt entered:
- Files selected:
- Files Fazah used:
- Result: Pass / Small Issue / Fail / Critical Fail
- Short note:

---

## Auditor variation

The auditor may vary the *phrasing or a single formatting ask* without breaking the Expect lines. Any
one of these substitutions is acceptable:

- Turn 4 ("put that in a table") may instead be "add a limitation" / "add a constraint of each".
- Turn 2's framing may be narrowed to "for first-year students" or "keep it under 200 words".
- Any follow-up may be reworded conversationally, as long as the underlying request (compare /
  realistic case / forgettable difference / table / 4 questions / student version / which deck /
  security note / harder / teacher key / scenario / verify) is preserved.

Do not vary: the target of 14 turns, the no-answers student turn, or the which-deck turn. All Expect
lines still apply under any allowed substitution.

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

For the complete workflow, see [Context Diagram](../misc/CONTEXT-DIAGRAM.md).
