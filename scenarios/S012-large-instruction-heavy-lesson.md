# S012 — Large, instruction-heavy lesson

## Tests

Fazah extracts many constraints packed into one large prompt, then sustains a demanding teacher's
run of targeted edits to the same Agile lesson — retiming, adding a task, expanding prep notes,
swapping the exit ticket, producing a handout and answer key — without dropping earlier constraints.

## Setup

- Start: New chat
- Select files: `Ch5 Agile SW Dev.pptx`
- Do not select: any other deck
- Turns: 8
- Auditor variation: Not allowed

---

## Turn 1

### Enter

```text
Build me a 45-minute lesson on Agile software development for an undergraduate class.
It must include:
- three measurable learning objectives
- a five-minute opening
- a 15-minute explanation
- a 10-minute group task
- a five-minute debrief
- a five-minute exit ticket
Use the Agile lecture only, and include teacher preparation notes.
```

### Expect

- Lesson plan includes every segment with the specified durations and exactly three measurable
  objectives, pitched for undergraduates.
- Content is drawn from the Agile deck only (`Ch5 Agile SW Dev.pptx`) — e.g. Agile Manifesto, XP
  practices, Scrum — and teacher preparation notes are present.
- No listed constraint is dropped or silently merged.

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
Shorten the explanation to 10 minutes.
```

### Expect

- Only the explanation segment changes to 10 minutes; other segments keep their durations.
- Segment structure and the three objectives from turn 1 are preserved.

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
Add a second group task.
```

### Expect

- Adds one more group task grounded in the Agile deck; the existing task is kept.
- Rest of the lesson (objectives, opening, debrief, exit ticket) is unchanged; timing is adjusted
  coherently rather than segments silently deleted.

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
Add more detailed teacher preparation notes.
```

### Expect

- Expands the teacher prep notes with more detail (materials, timing, likely misconceptions).
- Notes stay grounded in the Agile deck; the lesson body is not rewritten.

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
Swap the exit ticket for three short questions instead.
```

### Expect

- Replaces the exit-ticket segment with exactly three short Agile questions.
- Only the exit-ticket portion changes; objectives, tasks, and prep notes are preserved.

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
Make a student handout for this lesson.
```

### Expect

- Produces a student-facing handout drawn from the lesson (objectives, key Agile points, the tasks).
- Teacher-only material (prep notes, answers) is not exposed in the student handout.

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
Now make the answer key for those three questions separately.
```

### Expect

- Produces a separate answer key for the three questions from turn 5.
- Answers match those three questions; they are not folded back into the student handout.

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
Confirm this only used the Agile deck and nothing else.
```

### Expect

- Confirms the Agile deck (`Ch5 Agile SW Dev.pptx`) as the sole source.
- Does not claim any other file was used; no fabricated sources.

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
