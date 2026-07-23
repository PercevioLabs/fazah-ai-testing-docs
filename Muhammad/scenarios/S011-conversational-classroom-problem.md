# S011 — Conversational classroom problem

## Tests

Fazah recognizes intent from a natural, conversational teaching problem and sustains it into a
full pre-class package — explanation, activity, examples, handout, exit ticket, student version —
each step building on the same functional vs non-functional goal.

## Setup

- Start: New chat
- Select files: none
- Do not select: n/a
- Turns: 7
- Auditor variation: Not allowed

---

## Turn 1

### Enter

```text
ok so my students keep mixing up functional vs non-functional requirements, can u help me explain the difference before class
```

### Expect

- Gives a clear functional vs non-functional distinction grounded in Requirements content (Ch3):
  functional = services the system should provide / how it reacts to inputs; non-functional =
  constraints or quality attributes, often applying to the whole system.
- May note non-functional requirements can be more critical than functional ones.
- Explanation is teacher-usable and course-consistent.

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
now gimme a quick 2 min opening activity to check if they actually got it
```

### Expect

- Provides a short (~2 minute) opening activity that checks functional vs non-functional understanding.
- Builds on the turn 1 distinction rather than starting a new topic.
- Activity is classroom-ready with clear instructions the teacher can run immediately.

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
can u give me 3 quick examples of each so i can throw them on the board
```

### Expect

- Gives three functional and three non-functional examples, correctly sorted.
- Examples are course-consistent (e.g. Mentcare-style functional actions vs availability/timing/
  privacy constraints); does not mislabel one type as the other.

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
ok turn all that into a short one page handout for the students
```

### Expect

- Produces a short handout combining the definition and the examples from the earlier turns.
- Nothing new is invented beyond what was already covered; content stays consistent.
- Formatted for a single page and student-appropriate.

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
add a 3 question exit ticket at the end
```

### Expect

- Adds exactly three questions that check functional vs non-functional understanding.
- The handout content above is preserved; only the exit ticket is added.

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
now make a student version of the exit ticket w no answers
```

### Expect

- Produces the three exit-ticket questions with NO answers shown.
- Answer leakage into the student version = Critical fail.
- Same three questions as turn 5, just without answers.

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
oh also what source did this come from
```

### Expect

- Points to the Requirements deck (`Ch3 Req Eng.pptx`) as where functional vs non-functional is covered.
- No source was selected, so it is honest that it drew on course-consistent knowledge / that deck —
  it does not fabricate a specific file it never used.

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
