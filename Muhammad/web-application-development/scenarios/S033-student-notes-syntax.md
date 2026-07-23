# S033 — Student notes from the syntax deck, iterative build

## Tests

With only the syntax deck selected, Fazah turns the deck into student-facing notes, then sustains a
16-turn iterative build — strip teacher language, glossary, per-section summary boxes, self-check
questions with a separate key, case-sensitivity and semicolon notes, a `<?php ?>` example, a
processing-flow box, and a 2-page limit — all grounded in the same deck, keeping the student version
answer-free throughout.

## Setup

- Start: New chat
- Select files: `php_syntax_presentation.pptx`
- Do not select: any other deck
- Turns: 16
- Auditor variation: Not allowed

---

## Turn 1

### Enter

```text
make student facing notes from the syntax deck
```

### Expect

- Produces student-facing notes summarising php_syntax (tags, semicolons, case sensitivity, server-side processing).
- Grounded in `php_syntax_presentation.pptx`; no other deck.

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
take out any teacher facing language, its for students
```

### Expect

- Removes instructor-directed phrasing; the notes read as student-facing.
- Content is otherwise preserved.

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
add a glossary and keep it to 2 pages max
```

### Expect

- Adds a glossary of key terms and constrains the notes to ~2 pages.
- Only grounded terms (tag, statement, case-sensitive, server-side, etc.).

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
add a little summary box to each section
```

### Expect

- Adds a concise summary box per section.
- Stays within ~2 pages; content grounded.

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
add 3 self check qs, no answers shown
```

### Expect

- Adds exactly 3 self-check questions with NO answers in the student notes
  (answer-leakage check — leaked answers = Critical fail).
- Questions grounded in syntax facts.

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
make a teacher key for those 3, separate
```

### Expect

- Teacher key for the 3 self-check questions, delivered separately from the student notes.
- The student notes stay answer-free.

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
double check the student version has zero answers
```

### Expect

- Verifies the student notes contain no answers to the self-check questions (answer-leakage check).
- Confirms the key is the separate doc.

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
confirm which file this is from and who its for
```

### Expect

- Confirms source = `php_syntax_presentation.pptx` and audience = students.
- No unselected deck claimed.

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
add a note about case sensitivity
```

### Expect

- Adds a note that PHP is case-sensitive (e.g. `$age` ≠ `$Age`), grounded in the deck.
- Fits within the notes.

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
add a short example showing the <?php ?> tag
```

### Expect

- Adds a short, valid example using the canonical `<?php … ?>` tag.
- Grounded; consistent with the deck (notes it is the recommended tag).

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
make the wording simpler
```

### Expect

- Simplifies the wording for students; the facts are unchanged.
- Still grounded, still student-facing.

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
its over 2 pages, cut it down
```

### Expect

- Trims the content to fit ~2 pages while keeping the core syntax concepts + glossary + self-checks.
- Still answer-free.

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
confirm its 2 pages
```

### Expect

- Confirms the notes fit ~2 pages (or trims further to comply).
- Reports the length honestly.

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
add a box showing the processing flow (browser to server to browser)
```

### Expect

- Adds a box showing the flow: browser requests `.php` → server processes → HTML/CSS/JS sent → browser renders (from the deck).
- Grounded; the order is accurate.

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
add a 1 line note that statements end w/ a semicolon, but stay 2 pages
```

### Expect

- Adds a one-line note that PHP statements end with `;`; re-fits to ~2 pages if needed.
- Grounded; still answer-free.

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
final check — student version, no answers, 2 pages
```

### Expect

- Final student notes: no answers to the self-checks (answer-leakage check — leaked answers = Critical fail),
  ~2 pages, with glossary + summary boxes + processing-flow box present.
- The teacher key is kept separate.

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
