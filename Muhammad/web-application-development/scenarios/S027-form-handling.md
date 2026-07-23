# S027 — Form handling (action/method/name, $_GET vs $_POST, security)

## Tests

With only the forms deck selected, Fazah explains form handling on the deck's terms — the `action`,
`method`, and `name` attributes, `$_GET` vs `$_POST`, and the validate/sanitize security note — then
sustains a build with a code example, a trace, commented code, and teacher/student questions, all
grounded in `php_forms` without fabricating behaviour the deck does not state.

## Setup

- Start: New chat
- Select files: `php_forms_presentation.pptx`
- Do not select: any other deck
- Turns: 14
- Auditor variation: Not allowed

---

## Turn 1

### Enter

```text
explain form handling - action, method and name attributes, $_GET vs $_POST, and one security note
```

### Expect

- `action` = where the form data is sent; `method` = GET or POST; `name` = the field's identifier — per the deck.
- `$_GET` reads URL parameters, `$_POST` reads submitted form data; security note = never trust user
  input, always validate and sanitize.
- Grounded in the selected forms deck (grounding badge / php_forms under used sources).

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
add more detail on GET vs POST
```

### Expect

- GET = visible in the URL, bookmarkable/cached, ~2000-char limit, not for sensitive data, no file
  uploads; POST = not in the URL, no size limit, file uploads, secure — per the deck.
- Notes POST is the recommended method for forms.
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
give me a code example, a form plus the $_POST access
```

### Expect

- A valid `<form action="process.php" method="POST">` with an `<input name="…">` and a submit button,
  plus server-side access via `$_POST['…']` using the same field name.
- Attributes and superglobal match the deck; no invented functions or framework code.
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
walk through what happens when that $_POST line runs
```

### Expect

- Traces it correctly: the form submits to the `action` page; `$_POST['name']` reads the value of the
  field whose `name` attribute is `name` — the `name` attribute is the `$_POST` key.
- Reasoning is consistent with the example from Turn 3.
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
add comments to that code
```

### Expect

- Adds short comments to the example explaining `action`, `method`, `name`, and the `$_POST` access.
- The code stays valid and unchanged apart from the comments; nothing new is claimed.
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
make 5 qs from this
```

### Expect

- Exactly 5 questions drawn from the form-handling material above (attributes, `$_GET`/`$_POST`, GET
  vs POST, security), not new topics.
- Any answers given are consistent with the deck.
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
student version no answers
```

### Expect

- The same 5 questions, student-facing, with NO answers shown
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
add a teacher key
```

### Expect

- A teacher key with the correct answer + a short explanation for each of the 5 questions.
- Answers follow the deck; the student version stays answer-free.
- Still grounded in `php_forms`.

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
which deck is this from
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

## Turn 10  (continue the same chat)

### Enter

```text
make them harder
```

### Expect

- The 5 questions become harder while staying on form handling; still exactly 5, still answerable
  from the deck.
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
add a scenario q
```

### Expect

- Adds one scenario-framed question (e.g. a login form — GET or POST and why → POST; or which
  attribute names the field that becomes the `$_POST` key).
- The correct answer follows the deck; the existing 5 questions are kept.
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
add one q specifically on the name attribute
```

### Expect

- Adds one more question specifically on the `name` attribute (the field identifier that becomes the
  `$_GET`/`$_POST` key) — per the deck.
- The existing items are kept; only one is added, consistent with the current answer state so it does
  not leak an answer.
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
reorder easiest to hardest
```

### Expect

- The same questions (5 base + scenario + name-attribute item) reordered easiest → hardest; content
  unchanged, none added or dropped.
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
double check the count and nothing changed
```

### Expect

- Reports the current question count accurately (5 base + the 2 added items) and confirms the code
  example, trace, and security note are unchanged.
- No silent additions, drops, or contradictions.
- Still attributes everything to `php_forms` only.

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

For the complete workflow, see [Context Diagram](../misc/CONTEXT-DIAGRAM.md).
