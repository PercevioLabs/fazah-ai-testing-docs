# S028 — HTTP request/response synthesis, iterative build in Module 1

## Tests

With only Module 1 selected, Fazah synthesizes the HTTP layer of the deck — the request verbs,
response-code categories, request/response flow, and statelessness — then holds a long iterative build
into a table, quick-check questions, teacher/student versions, a networking-command note, and a
scenario item, all grounded in Module 1 without claiming a Module 2 that does not exist.

## Setup

- Start: New chat
- Select files: `Module 1 - Computer Network for Web Developer.pptx`
- Do not select: any other deck
- Turns: 18
- Auditor variation: Not allowed

---

## Turn 1

### Enter

```text
what are the http request verbs
```

### Expect

- Names GET (normal resource fetching), POST (submitting forms, payload attached), UPDATE (updating a
  resource), DELETE (deleting) — per Module 1.
- Grounded in the selected Module 1 deck (grounding badge / Module 1 under used sources).
- Does not invent extra verbs as if from the deck.

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
what do the response code categories mean
```

### Expect

- 1xx = informational, 2xx = success, 3xx = redirection, 4xx = client-side errors (e.g. wrong page),
  5xx = server-side errors — per Module 1.
- Reuses the same source; does not drift to a different deck.
- Still grounded in Module 1.

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
add that theyre 3 digits n the first digit is the category
```

### Expect

- Notes that a response code is 3 digits and the first digit marks the category — per Module 1.
- Consistent with Turn 2; nothing contradicted.
- Does not assert specific numeric codes (e.g. 200, 404) as verbatim deck content.

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
how does request/response actually work
```

### Expect

- Client sends a request to the server; the server sends back a response — HTTP works in
  request/response pairs, per Module 1.
- Ties to the verbs (a request uses a verb) built up above.
- Still grounded in Module 1.

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
and what does stateless mean
```

### Expect

- HTTP is stateless: each request is handled separately/independently, with no memory of previous
  requests — per Module 1.
- Consistent with the request/response framing from Turn 4.
- Still grounded in Module 1.

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
put the verbs n their use in a table
```

### Expect

- A table pairing each verb (GET, POST, UPDATE, DELETE) with its use from Turn 1.
- No new verbs added and no content changed — only reformatted.
- Still grounded in Module 1.

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
turn that into 3 student quick check qs
```

### Expect

- Exactly 3 quick-check questions drawn from the verb/response material above, not new topics.
- Items are answerable from the deck.
- Still grounded in Module 1.

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
add a teacher key
```

### Expect

- An answer key for the same 3 questions (keeps the set, adds correct answers + short explanations).
- Answers follow the deck (GET fetches; POST submits forms; 4xx = client error, etc.).
- Still grounded in Module 1.

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
student version no answers
```

### Expect

- The same 3 questions, student-facing, with NO answers shown
  (answer-leakage check — leaked answers = Critical fail).
- The teacher key from Turn 8 is preserved; only the student copy is produced.

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
make the quick check mcq
```

### Expect

- The 3 quick-check questions become multiple choice, still student-facing with NO correct option
  marked (answer-leakage check — leaked answers = Critical fail).
- Options stay on the deck's material (verbs, response categories); count stays at 3.
- Still grounded in Module 1.

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
add a q on status codes
```

### Expect

- Adds one more question on the response-code categories (e.g. what 4xx vs 5xx means).
- The existing 3 items are kept; only one is added, consistent with the current student (no-answers)
  state so it does not leak an answer.
- Still grounded in Module 1.

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
add a note on ping traceroute n nslookup
```

### Expect

- Adds a short note: `ping` checks connectivity, `traceroute`/`tracert` traces packets, `nslookup`
  does a DNS lookup — per Module 1.
- Extends the material; the verbs, codes, and quiz above are kept.
- Still grounded in Module 1.

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
make them harder
```

### Expect

- The quick-check questions become harder while staying on the HTTP/Module 1 material; count is
  preserved (3 base + the status-code item).
- Any current student (no-answers) copy is not made to leak answers.
- Still grounded in Module 1.

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
reorder easiest to hardest
```

### Expect

- The same questions reordered easiest → hardest; content unchanged, none added or dropped.
- Still grounded in Module 1.

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
confirm this is all from module 1
```

### Expect

- Names Module 1 (`Module 1 - Computer Network for Web Developer.pptx`) as the source used throughout.
- Does not claim a Module 2 (which does not exist) or any other unselected deck, and does not hedge
  that it had no source.

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
add a scenario q
```

### Expect

- Adds one scenario-framed question (e.g. submitting a login form uses which verb → POST; a browser
  requests a page that doesn't exist → which category → 4xx).
- The correct answer follows the deck; the existing questions are kept.
- Still grounded in Module 1.

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
double check the count
```

### Expect

- Reports the current question count accurately (3 base + status-code item + scenario item) and
  confirms the verbs, response categories, and command note are unchanged.
- No silent additions, drops, or contradictions.
- Still grounded in Module 1.

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
list everything weve built
```

### Expect

- Recaps the artifacts: the verbs + uses, response-code categories (3-digit / first-digit note),
  request/response and stateless explanations, the verb table, the quiz (teacher key, student version,
  MCQ, status-code and scenario items), and the ping/traceroute/nslookup note.
- Nothing new is introduced; the recap matches earlier turns.
- Still attributes everything to Module 1 only.

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
