# S013 — Auditor adds one instruction (PHP syntax)

## Tests

A precise teacher builds a small syntax explainer → summary → check kit on the selected syntax deck,
and the auditor folds in exactly one extra instruction on the opening turn. Fazah must honour the added
constraint alongside the main goal, keep the student and teacher versions split, and stay grounded in
php_syntax.

## Setup

- Start: New chat
- Select files: `php_syntax_presentation.pptx`
- Do not select: any other deck
- Turns: 12
- Auditor variation: Allowed (see the Auditor variation section below)

---

## Turn 1

### Enter

```text
Explain PHP tags, statements, and case sensitivity.
```

(Then add exactly one instruction — see the Auditor variation section.)

### Expect

- Explains canonical `<?php ... ?>` tags (short `<? ?>` needs `short_open_tag=on`), statements ending
  with `;`, and case sensitivity (`$age` differs from `$Age`) — matching php_syntax.
- Honours the one added instruction from the variation without dropping the core explanation.
- No invented citation to a deck that was not selected.

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
Give a short example that shows all three.
```

### Expect

- A valid PHP snippet showing the `<?php ?>` tags, a `;`-terminated statement, and case sensitivity.
- Consistent with php_syntax; the example runs as written.

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
Turn that into a short student summary.
```

### Expect

- A concise, student-friendly summary of tags, statements, and case sensitivity.
- Grounded in php_syntax; no new topics introduced.

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
Add a 3 question check for understanding.
```

### Expect

- Exactly 3 questions covering tags, statements, and case sensitivity, each with a correct answer.
- Grounded in php_syntax; nothing outside the deck.

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
Now a student version with no answers.
```

### Expect

- The same 3 questions in a student-facing version with NO answers shown
  (answer-leakage check — leaked answers = Critical fail).

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
Which file did you use?
```

### Expect

- Names the syntax deck (`php_syntax_presentation.pptx`) as the source used throughout.
- Does not claim a different or unselected deck.

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
Add a note on the processing flow — browser requests the .php, server processes it, HTML is sent back.
```

### Expect

- Adds a note on the flow: browser requests the `.php` file → server processes it → HTML/CSS/JS is sent
  back → browser renders — matching php_syntax.
- Does not overwrite the existing summary or questions.

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
Make the 3 questions harder.
```

### Expect

- The 3 questions become harder (e.g. spot the case-sensitivity bug, which tag needs config); still 3.
- Still grounded in php_syntax.

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
Give me the teacher key with explanations.
```

### Expect

- A teacher key with the correct answer + short explanation for each of the 3 questions.
- The student version from Turn 5 stays answer-free.

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
Verify there are exactly 3 questions and one correct answer each.
```

### Expect

- Confirms exactly 3 questions, each with exactly one correct answer; flags any exception honestly.
- Does not silently add or drop questions.

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
Reorder them easiest to hardest.
```

### Expect

- The same 3 questions reordered easiest → hardest; content unchanged, none added or dropped.

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
Give me a final inventory of everything.
```

### Expect

- A clear inventory: explanation, example, student summary, processing-flow note, 3 questions
  (student + teacher key).
- Counts and pieces match what was produced; the added variation instruction is still reflected.

### Record

- Actual prompt entered:
- Files selected:
- Files Fazah used:
- Result: Pass / Small Issue / Fail / Critical Fail
- Short note:

---

## Auditor variation

Add or change one realistic instruction. Record exactly what you entered. Do not change the scenario's
main goal.

Examples:

- Present the explanation as a table.
- Add one worked example.
- Pitch it for first-year students.
- Keep it under 200 words.

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
