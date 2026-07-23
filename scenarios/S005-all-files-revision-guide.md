# S005 — All files selected, revision guide built out across many turns

## Tests

With all five decks selected, Fazah builds a lecture-organized revision guide, then sustains a long
workflow — cross-chapter links, added definitions, a condensed version, a cumulative quiz with
teacher and student versions, and a glossary — preserving prior work at each step and grounding every
section in the right deck.

## Setup

- Start: New chat
- Select files: all five decks (`Ch1 Introduction.pptx`, `Ch2 SW Processes.pptx`, `Ch3 Req Eng.pptx`,
  `Ch4 Testing.pptx`, `Ch5 Agile SW Dev.pptx`)
- Do not select: n/a
- Turns: 9
- Auditor variation: Not allowed

---

## Turn 1

### Enter

```text
Create a concise revision guide for this course, organized by lecture.
```

### Expect

- Organized by the five lectures/decks (one section per deck).
- Each section hits that deck's key points: Ch1 attributes of good software / ethics; Ch2 process
  models (waterfall, incremental); Ch3 functional vs non-functional requirements; Ch4 testing stages
  / V&V; Ch5 agile, XP, Scrum.
- Used sources reflect all five decks.

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
Add five cross-chapter connections without rewriting the guide.
```

### Expect

- Exactly five cross-chapter connections added; the Turn 1 guide is preserved (selective expansion).
- Connections are real per the content map (e.g. TDD in Ch4 & Ch5; prototyping in Ch2 & Ch3;
  plan-driven vs agile in Ch2 & Ch5; user stories in Ch3 & Ch5; V&V in Ch2 & Ch4).

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
Add two key definitions to each lecture section.
```

### Expect

- Two definitions per lecture section (ten in total), each grounded in that deck (e.g. Ch1 software /
  software engineering; Ch2 software process / prototype; Ch3 functional / non-functional; Ch4
  verification / validation; Ch5 refactoring / Scrum).
- The existing guide and the five connections from Turns 1–2 are preserved.

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
Make a one-page condensed version of the guide.
```

### Expect

- A single-page condensation of the built-up guide, keeping all five lecture sections.
- Substance is condensed, not replaced with new topics.

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
Generate a 10-question cumulative quiz that spans all five decks.
```

### Expect

- Exactly ten questions, collectively covering all five decks (not concentrated on one chapter).
- Each question is grounded in course material; used sources span the five decks.

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
Give me the teacher answer key for that quiz.
```

### Expect

- An answer key for the same ten questions from Turn 5 (same questions, now with answers).
- Answers are supported by the decks; the question set is unchanged.

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
Now a student version of the quiz with no answers.
```

### Expect

- The same ten questions in a student-facing version with NO answers shown
  (answer-leakage check — leaked answers = Critical fail).
- The teacher key from Turn 6 is preserved as its own version.

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
Add a glossary to the revision guide.
```

### Expect

- A glossary of course terms drawn from the five decks is added to the guide.
- The guide, connections, definitions, and quizzes built earlier are preserved.

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
Summarize what we built and which files fed each section.
```

### Expect

- An inventory of the artifacts actually produced (guide, connections, definitions, condensed
  version, quiz, teacher key, student version, glossary) — no fabricated extras.
- Each section is attributed to the correct deck(s); no source is invented.

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
