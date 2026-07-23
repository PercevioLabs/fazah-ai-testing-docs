# S005 — All files selected, cross-topic revision guide

## Tests

With all 15 decks selected, Fazah builds a topic-organised revision guide and iterates on it over a
long arc — condensing, adding cross-topic connections, a 10-question cumulative quiz, glossary,
networking and architecture sections — staying grounded across the whole course, never fabricating
diagram-only content, and correctly mapping each section back to its source file.

## Setup

- Start: New chat
- Select files: all 15 decks
- Do not select: — (all 15 decks selected)
- Turns: 20
- Auditor variation: Not allowed

---

## Turn 1

### Enter

```text
make a concise revision guide organized by topic
```

### Expect

- A topic-organised revision guide spanning the selected decks (networks, architecture, and the PHP
  topics).
- Grounded across the 15 decks; no invented topics; diagram-only content (OSI / TCP-IP layers) not
  fabricated as verbatim text.

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
no too long, 2-3 bullets per topic max
```

### Expect

- Condenses each topic to 2-3 bullets while keeping every topic.
- Still grounded; nothing dropped or invented.

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
add 5 cross-topic connections at the end
```

### Expect

- Lists 5 connections such as HTTP GET/POST verbs ↔ `$_GET`/`$_POST`, dynamic pages need an
  interpreter + database, and syntax underpins every PHP topic — drawn from the course's connections.
- Grounded; accurate.

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
give me 2 key points per topic
```

### Expect

- Exactly 2 key points per topic, each grounded in the respective deck.
- No topic invented or omitted.

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
add one tiny example per php topic
```

### Expect

- One short valid PHP example per PHP topic (e.g. `strlen`, `foreach`, `===`), consistent with the
  decks.
- No examples invented for the concept-only modules beyond what they cover.

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
ok condense the whole thing to one page
```

### Expect

- A one-page condensed version retaining all topics.
- Still grounded; nothing invented.

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
add learning objectives at the top
```

### Expect

- Objectives derived from the covered topics; grounded, not invented.

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
now a 10 q cumulative quiz across topics
```

### Expect

- Exactly 10 questions spanning multiple topics, each with a correct answer supported by the decks.

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
make 2 of them write-the-code / scenario
```

### Expect

- Exactly two of the 10 become write-the-code / scenario questions; the rest unchanged.
- Still 10, still grounded.

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
make 3 of them harder
```

### Expect

- Exactly three of the 10 become harder; the rest preserved.
- Still 10.

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
check each q has exactly 1 correct answer
```

### Expect

- Confirms each of the 10 has a single correct answer; fixes any ambiguity.
- Count stays at 10.

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
reorder easiest to hardest
```

### Expect

- The same 10 questions reordered easiest → hardest; none added or dropped.

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
teacher key w short explanations
```

### Expect

- Teacher key: correct answer + short explanation for each of the 10.

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
student version, no answers
```

### Expect

- The same 10 questions, student-facing, with NO answers shown
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
add a glossary of php terms
```

### Expect

- Glossary of PHP terms (e.g. superglobal, concatenation, casting, fall-through, associative array),
  grounded in the decks.
- No invented definitions.

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
add a networking / http section from module 1
```

### Expect

- Adds a networking / HTTP section (layered OSI / TCP-IP, IP = 32-bit / 4 octets, DNS, HTTP stateless
  request/response, verbs, status codes) from Module 1.
- Grounded; the diagram-only layer lists are not fabricated verbatim.

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
and a web architecture section from module 3
```

### Expect

- Adds an architecture section: client-server, static vs dynamic (dynamic adds interpreter + DB), MVC
  (Model / View / Controller) — from Module 3.
- Grounded; no fabrication.

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
verify every topic is covered, nothing missing
```

### Expect

- Confirms all 15 decks' topics are represented in the guide; flags any gaps honestly rather than
  padding.

### Record

- Actual prompt entered:
- Files selected:
- Files Fazah used:
- Result: Pass / Small Issue / Fail / Critical Fail
- Short note:

---

## Turn 19  (continue the same chat)

### Enter

```text
give me an inventory — which file fed each section
```

### Expect

- Maps each section to its source deck (e.g. HTTP → Module 1, MVC → Module 3, quotes → php_strings).
- Attribution accurate; no file misassigned or invented.

### Record

- Actual prompt entered:
- Files selected:
- Files Fazah used:
- Result: Pass / Small Issue / Fail / Critical Fail
- Short note:

---

## Turn 20  (continue the same chat)

### Enter

```text
last thing — confirm the student quiz has no answers and its still 10 qs
```

### Expect

- Confirms the student version has NO answers and the quiz is still 10 questions
  (count + answer-leakage check).

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
