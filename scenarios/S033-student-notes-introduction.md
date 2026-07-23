# S033 — Student notes from the Introduction deck: audience + answer separation

## Tests

Sustained multi-turn workflow on ONE set of student notes: Fazah writes student-facing notes, strips
teacher language, adds a glossary and holds to two pages, adds per-section summaries and answer-free
self-check questions, then produces a separate teacher key — keeping the student version answer-free and
the audience clearly student throughout.

## Setup

- Start: New chat
- Select files: `Ch1 Introduction.pptx`
- Do not select: any other deck
- Turns: 8
- Auditor variation: Not allowed

---

## Turn 1

### Enter

```text
Create student-facing notes from this lecture.
```

### Expect

- Student-facing notes are produced (written for students to read).
- Content is grounded in the Introduction deck (e.g. what software engineering is, four attributes of
  good software, four process activities, application types, ethics), not generic material.
- The tone/level suits students.

### Record

- Actual prompt entered:
- Files selected:
- Files Fazah used:
- Result: Pass / Small Issue / Fail / Critical Fail
- Short note:

---

## Turn 2   (continue the same chat; keep `Ch1 Introduction.pptx` selected)

### Enter

```text
Remove any teacher-facing language.
```

### Expect

- Teacher-facing language (e.g. "tell students", lesson-plan asides, instructor notes) is removed.
- The student content itself is preserved — only audience framing changes.
- The result reads clearly as student-facing (audience-leakage check).

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
Add a glossary and limit the final version to two pages.
```

### Expect

- A glossary of key terms (grounded in the deck) is added.
- The final version fits roughly two pages.
- It stays student-facing with no teacher-only notes reintroduced (audience-leakage check).

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
Add a summary box to each section.
```

### Expect

- A short summary box is added per section, grounded in the deck.
- The glossary and prior notes are preserved; still student-facing.
- The document stays close to the two-page limit (or Fazah flags the trade-off).

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
Add three self-check questions with no answers.
```

### Expect

- Exactly three self-check questions are added, grounded in the deck, with NO answers shown.
- The notes, glossary, and summary boxes are preserved.
- Answers do not appear anywhere in the student notes (answer-leakage check).

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
Now make a teacher key for those questions.
```

### Expect

- A separate teacher key answers the three self-check questions, grounded in the deck.
- The key matches the questions from Turn 5.
- The student notes remain answer-free (the key is a separate document).

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
Double-check the student version still has no answers in it.
```

### Expect

- Fazah confirms the student notes contain no answers to the self-check questions.
- The confirmation reflects the actual student document, not the teacher key.
- Any leaked answer found is corrected (answer-leakage check).

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
Confirm which file you used and who the notes are written for.
```

### Expect

- Fazah names `Ch1 Introduction.pptx` as the source and does not claim another deck.
- It confirms the notes are student-facing (audience is students).
- The summary reflects the actual documents produced (student notes + teacher key).

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

For the complete workflow, see [Context Diagram](../CONTEXT-DIAGRAM.md).
