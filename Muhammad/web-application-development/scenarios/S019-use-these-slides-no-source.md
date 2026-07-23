# S019 — "Use these slides" with nothing selected

## Tests

A teacher says "use these slides and make 5 questions" but no deck is selected. Fazah must ask which
slides rather than guessing or inventing a source, then — once `php_forms` is selected — build and
refine a forms quiz grounded in that deck through a long workflow, keeping the student version
answer-free.

## Setup

- Start: New chat
- Select files: none at Turn 1; from Turn 2 select `php_forms_presentation.pptx`
- Do not select: any other deck
- Turns: 14
- Auditor variation: Not allowed

---

## Turn 1

### Enter

```text
use these slides and make 5 questions
```

### Expect

- No deck is selected, so Fazah asks which slides / deck to use (or states nothing is selected).
- Does **NOT** invent a source, guess a topic, or produce five questions from nothing.

### Record

- Actual prompt entered:
- Files selected:
- Files Fazah used:
- Result: Pass / Small Issue / Fail / Critical Fail
- Short note:

---

## Turn 2  (continue the same chat — select `php_forms_presentation.pptx`)

### Enter

```text
these ones
```

### Expect

- Grounds in the now-selected `php_forms` deck and produces five questions on forms
  (`<form action method>`, `$_GET`/`$_POST`, GET vs POST, validate/sanitize).
- No answers shown yet; no facts outside php_forms.

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
add the answers
```

### Expect

- One correct answer per question, each supported by php_forms (e.g. `$_POST` = form data; POST
  recommended for forms; always validate and sanitize).
- Still exactly five questions.

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
turn q2 into a scenario question
```

### Expect

- Only question 2 becomes scenario-based (e.g. a login form — pick GET or POST and say why); the
  other four are unchanged.
- Still five, still php_forms.

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
reorder them foundational to advanced
```

### Expect

- The same five questions reordered foundational → advanced; none added or dropped, content unchanged.

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
now a student version, no answers
```

### Expect

- The same five questions in a student-facing version with NO answers shown
  (answer-leakage check — leaked answers = Critical fail).

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
which deck did u use
```

### Expect

- Names `php_forms_presentation.pptx` as the source used throughout.
- Does not claim the unnamed "these slides" from Turn 1 or any deck that was never selected.

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
add a GET vs POST question, so 6
```

### Expect

- Adds one GET vs POST question grounded in php_forms (GET visible in URL / ~2000-char limit / not for
  sensitive data; POST not in URL / no size limit / file uploads / secure).
- Count is now six; earlier questions preserved.

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
teacher key w explanations
```

### Expect

- A teacher key with the correct answer + a short explanation for each of the six, grounded in php_forms.
- The student version stays answer-free.

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
make 2 of them harder
```

### Expect

- Exactly two questions become harder; the other four are preserved. Still six, still grounded.

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
update the student version to match
```

### Expect

- Student version reflects all six current questions including the GET-vs-POST add and the harder items.
- Still NO answers shown (answer-leakage check — leaked answers = Critical fail).

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
verify its 6 questions
```

### Expect

- Confirms exactly six questions across both versions and the key.
- No content changed while verifying.

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
check each has exactly one right answer
```

### Expect

- Confirms each of the six has a single correct answer; flags any that don't.
- No new fabricated content introduced during the check.

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
quick inventory of what we got
```

### Expect

- Lists what was built: a 6-question forms quiz, a student version (no answers), and a teacher key.
- Names the single source: `php_forms_presentation.pptx`.

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
