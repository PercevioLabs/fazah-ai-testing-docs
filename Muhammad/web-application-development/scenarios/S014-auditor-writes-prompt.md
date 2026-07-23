# S014 — Auditor writes the opening prompt (HTTP for beginners)

## Tests

The auditor composes the opening message in their own words, aiming to get Fazah to explain the HTTP
request/response cycle for beginners, with Module 1 selected. Fazah must ground the whole arc in
Module 1 — the deck's own verbs and status-code bands — keep an analogy as a teaching device (not a
fabricated deck quote), and split the student and teacher materials.

## Setup

- Start: New chat
- Select files: `Module 1 - Computer Network for Web Developer.pptx`
- Do not select: any other deck
- Turns: 12
- Auditor variation: Allowed (see the Auditor variation section below)

---

## Turn 1

### Enter

Write your own opening message here — in your own words, ask Fazah to explain the HTTP request/response
cycle for complete beginners. Keep it casual, the way you would actually type it. Record the exact
wording you used in the Record block below. (This is a variation scenario — you may also fold in the one
allowed instruction from the Auditor variation section.)

### Expect

- Explains HTTP as the main web protocol, stateless, working in request/response pairs
  (client sends a request → server sends a response) — matching Module 1.
- Grounded in Module 1; no invented citation to a deck that was not selected.
- Pitched for beginners, honouring however the auditor's own wording framed it.

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
can u add an analogy to make it click
```

### Expect

- Adds a plain-language analogy for request/response (e.g. asking a question and getting an answer back).
- The analogy is presented as a teaching device, not attributed as a verbatim quote from the deck.

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
list the verbs plainly — GET POST UPDATE DELETE
```

### Expect

- Lists the deck's four verbs: GET (fetch a resource), POST (submit a form / payload), UPDATE, DELETE.
- Uses the deck's set exactly; does not substitute general-knowledge verbs like PUT/PATCH that are not in Module 1.

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
make 4 beginner questions
```

### Expect

- Exactly 4 beginner-level questions on HTTP request/response and the verbs, each with a correct answer.
- Grounded in Module 1; nothing outside the deck.

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
student version pls, no answers
```

### Expect

- The same 4 questions in a student-facing version with NO answers shown
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
which file is this from
```

### Expect

- Names Module 1 (`Module 1 - Computer Network for Web Developer.pptx`) as the source used throughout.
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
add a note on the status codes, 1xx through 5xx
```

### Expect

- Adds a note on the status-code bands: 1xx informational, 2xx success, 3xx redirection, 4xx client-side
  errors, 5xx server-side errors — matching Module 1.
- Does not overwrite the earlier explanation or questions.

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
make it simpler
```

### Expect

- Simplifies the wording for beginners while keeping the request/response, verbs, and status-code facts intact.
- Still grounded in Module 1; no facts changed to become incorrect.

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
teacher key please
```

### Expect

- A teacher key with the correct answer + short explanation for each of the 4 questions.
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
verify its 4 questions with one right answer each
```

### Expect

- Confirms exactly 4 questions, each with exactly one correct answer; flags any exception honestly.
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
redo the student version, make sure no answers show
```

### Expect

- Re-issues the 4 questions as a student version with NO answers or explanations exposed
  (answer-leakage check — leaked answers = Critical fail).

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
give me a final list of everything
```

### Expect

- A clear inventory: explanation, analogy, verb list, status-code note, 4 questions (student + teacher key).
- Counts and pieces match what was produced; the variation instruction is still reflected.

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

- Change the audience (e.g. non-technical staff).
- Keep it under a minute to read.
- Use exactly one analogy.
- Make the tone more formal.

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
