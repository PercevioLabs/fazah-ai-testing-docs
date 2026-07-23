# S003 — Wrong file selected, topic conflict

## Tests

The loops deck is selected but the teacher asks about form handling — a topic that deck does not
cover. Fazah should flag the mismatch honestly instead of fabricating form content and attributing it
to the loops deck, recommend the right file, then — once the forms deck is selected — sustain a long,
corrective workflow entirely grounded in the forms deck.

## Setup

- Start: New chat
- Select files: `php_loops_presentation.pptx` (deliberately the wrong deck for this topic)
- Do not select: `php_forms_presentation.pptx` at the start (selected mid-chat at Turn 3)
- Turns: 16
- Auditor variation: Not allowed

---

## Turn 1

### Enter

```text
explain form handling using the selected slides
```

### Expect

- The selected deck (`php_loops_presentation.pptx`) covers `while` / `do…while` / `for` / `foreach`,
  not form handling — Fazah flags the mismatch honestly.
- Does NOT fabricate form content and attribute it to the loops deck.
- Offers to switch to the forms deck or asks which file to use.

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
ok which file shd i use for forms
```

### Expect

- Recommends the forms deck (`php_forms_presentation.pptx`) as the right source for form handling.
- Does not invent a nonexistent file.

### Record

- Actual prompt entered:
- Files selected:
- Files Fazah used:
- Result: Pass / Small Issue / Fail / Critical Fail
- Short note:

---

## Turn 3  (continue the same chat — now select php_forms and deselect php_loops)

### Enter

```text
cool i selected it. explain forms — action, method, name
```

### Expect

- Explains `<form action method>` + `<input name>`: action = where to send, method = GET or POST,
  name = field id — matching the forms deck.
- Now grounded in `php_forms_presentation.pptx`, not the loops deck.

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
whats $_GET and $_POST
```

### Expect

- `$_GET` = URL params, `$_POST` = form data (superglobals) — matching the deck.
- Still grounded in the forms deck.

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
get vs post — when do i use which
```

### Expect

- GET: visible in URL, bookmarkable, ~2000-char limit, not for sensitive data, no file uploads.
- POST: not in URL, no size limit, file uploads, secure for passwords; recommended for forms = POST.
- Grounded in the forms deck.

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
gimme a code example — a form that posts to process.php
```

### Expect

- Valid HTML form: `<form action="process.php" method="POST">` with a named input + submit,
  consistent with the deck.
- No invented PHP; grounded in the forms deck.

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
show how process.php reads the username field, trace it
```

### Expect

- `$_POST["username"]` accesses the value submitted for `name="username"`; trace is consistent with
  the form from Turn 6.
- Grounded in the forms deck; no fabrication.

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
put get vs post in a comparison table
```

### Expect

- Table contrasting GET vs POST on URL visibility, size limit (~2000 chars vs none),
  caching / history / bookmarkable, security, and file uploads — matching the deck.

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
make 5 student qs on forms, no answers
```

### Expect

- Exactly 5 student-facing questions on forms with NO answers shown
  (answer-leakage check — leaked answers = Critical fail).
- Grounded in the forms deck.

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
teacher key for those w explanations
```

### Expect

- Teacher key: correct answer + short explanation for each of the 5; the student version stays
  answer-free.

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
make one of them scenario based
```

### Expect

- Exactly one of the 5 becomes a scenario question; the others unchanged.
- Still 5, still grounded in the forms deck.

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
swap the weakest q for one on validate/sanitize
```

### Expect

- Replaces one question with a validate-and-sanitize question (never trust user input) — grounded in
  the deck's security point.
- Count stays at 5.

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
reorder them easy to hard
```

### Expect

- The same 5 questions reordered easiest → hardest; none added or dropped.

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
regen the student version so no answers slip in
```

### Expect

- Updated 5-question student version with NO answers after the edits
  (answer-leakage check — leaked answers = Critical fail).

### Record

- Actual prompt entered:
- Files selected:
- Files Fazah used:
- Result: Pass / Small Issue / Fail / Critical Fail
- Short note:

---

## Turn 15  (continue the same chat)

### Enter

```text
which file did you end up using for all the form stuff
```

### Expect

- Names the forms deck (`php_forms_presentation.pptx`) as the source.
- Does not claim the loops deck was used for the form content.

### Record

- Actual prompt entered:
- Files selected:
- Files Fazah used:
- Result: Pass / Small Issue / Fail / Critical Fail
- Short note:

---

## Turn 16  (continue the same chat)

### Enter

```text
and none of this came from the loops deck right
```

### Expect

- Confirms the loops deck (`php_loops_presentation.pptx`) was not used for the form material; only the
  forms deck was.
- Attribution accurate; no fabrication.

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
