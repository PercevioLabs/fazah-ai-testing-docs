# S012 — Large, instruction-heavy lesson on web architecture

## Tests

The teacher opens with a single dense, demanding spec for a timed 45-minute lesson, then drives 17 more
tightening turns. Fazah must honour every constraint from the first prompt, reconcile the timing when a
segment is shortened, keep the student and answer-key materials split, and stay grounded strictly in
Module 3 — including honesty about the diagram-only slides.

## Setup

- Start: New chat
- Select files: `Module 3- Understanding Web Application Architecture.pptx`
- Do not select: any other deck
- Turns: 18
- Auditor variation: Not allowed

---

## Turn 1

### Enter

```text
I need a full 45 min lesson on web application architecture — client-server, static vs dynamic, and MVC — for undergrads. It must have 3 measurable objectives, a 5 min opening, 15 min explanation, 10 min activity, 5 min debrief, and a 5 min exit ticket. Use Module 3 only. Include teacher prep notes.
```

### Expect

- Produces a lesson with all requested parts: 3 measurable objectives, opening, explanation, activity,
  debrief, exit ticket, and teacher prep notes.
- Content grounded in Module 3 only (client-server, static vs dynamic, MVC roles); no other deck cited.
- The named segments total 40 min against the stated 45 — a strong response allocates or flags the
  5-minute gap rather than silently claiming 45.

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
shorten the explanation to 10 min
```

### Expect

- The explanation segment becomes 10 min; other segments are preserved.
- Explanation still covers client-server, static vs dynamic, and MVC at a shorter depth.

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
the timing doesnt add to 45 anymore, recheck it and fix
```

### Expect

- Reports the honest current total (segments now sum to 35 after the cut) and reconciles it to 45.
- Adjusts segment minutes transparently rather than asserting a total the parts do not reach.

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
add a 2nd activity
```

### Expect

- Adds a second activity grounded in Module 3; the first activity is kept.
- Re-checks the schedule so the added time is accounted for in the total.

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
add teacher talking points for the explanation part
```

### Expect

- Adds teacher talking points for the explanation, drawn from Module 3 (static = web server + file
  system, dynamic adds interpreter + database, MVC role split).
- Does not overwrite the existing prep notes.

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
need more prep notes
```

### Expect

- Expands the teacher prep notes with more Module 3 grounded detail.
- No fabricated content pulled from diagram-only slides or outside the deck.

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
swap the exit ticket for 3 short questions
```

### Expect

- Replaces the exit ticket with exactly 3 short questions on Module 3 content.
- Each question has a defensible correct answer; other lesson parts are unchanged.

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
make a student handout
```

### Expect

- A student-facing handout of the lesson content (client-server, static vs dynamic, MVC).
- Does NOT include the answers to the 3 questions (answer-leakage check — leaked answers = Critical fail).

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
put the answer key on a separate sheet
```

### Expect

- A separate answer key with the correct answer + brief explanation for each of the 3 questions.
- The student handout stays answer-free.

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
add an MVC role matching activity — Model / View / Controller
```

### Expect

- A matching activity pairing Model / View / Controller with their roles: Model = data logic
  (INSERT/UPDATE/LIST/DELETE), View = HTML/CSS frontend, Controller = business logic that glues view and model.
- Roles match Module 3 exactly; no invented responsibilities.

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
make the objectives measurable, start each with an action verb
```

### Expect

- The 3 objectives are rewritten to start with observable action verbs (e.g. identify, describe, distinguish).
- They still map to Module 3 content; count stays 3.

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
add a 2 min recap at the end
```

### Expect

- Adds a ~2 min recap segment; the schedule is re-totalled to stay coherent.
- Recap summarises the Module 3 points already taught, nothing new.

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
give me a short revision sheet for students
```

### Expect

- A concise student revision sheet covering client-server, static vs dynamic, and MVC roles.
- No quiz answers embedded (answer-leakage check — leaked answers = Critical fail).

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
student version of the 3 questions, no answers
```

### Expect

- The 3 short questions in a student-facing version with NO answers shown
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
make the whole lesson fit one printable page for me
```

### Expect

- Condenses the teacher-facing lesson into a one-page printable layout without dropping required parts
  (objectives, timed segments, activities, prep notes).
- Still Module 3 grounded; the separate answer key stays separate.

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
confirm this only uses Module 3, nothing else
```

### Expect

- Confirms the lesson is grounded solely in Module 3.
- Does not claim any other deck; is honest that some Module 3 slides are diagram-only.

### Record

- Actual prompt entered:
- Files selected:
- Files Fazah used:
- Result: Pass / Small Issue / Fail / Critical Fail
- Short note:

---

## Turn 17  (continue the same chat)

### Enter

```text
which part of Module 3 backs each section
```

### Expect

- Maps each lesson section to the Module 3 topic it draws on (client-server, static vs dynamic, MVC roles).
- Does not over-claim precise slide text for the diagram-only architecture slides.

### Record

- Actual prompt entered:
- Files selected:
- Files Fazah used:
- Result: Pass / Small Issue / Fail / Critical Fail
- Short note:

---

## Turn 18  (continue the same chat)

### Enter

```text
give me a final inventory of everything
```

### Expect

- A clear inventory: 3 measurable objectives, timed segments totalling 45 min, 2 activities, MVC
  matching activity, recap, 3 questions (student + separate key), student handout, revision sheet, prep notes.
- Counts and pieces match what was actually produced; nothing invented.

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
