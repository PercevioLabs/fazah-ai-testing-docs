# S022 — "Same sources as before" in a brand-new chat

## Tests

In a fresh chat with no prior context, the teacher says "use the same sources as before". Fazah must
not invent or claim any earlier source (there are none in a new chat) — it should ask which deck or
say nothing is selected. Once `php_loops` is selected it builds and refines a loops quiz grounded
there, correctly naming the one source and keeping the student version answer-free.

## Setup

- Start: NEW chat (fresh — no prior conversation, no carried-over sources)
- Select files: none at Turn 1; from Turn 2 select `php_loops_presentation.pptx`
- Do not select: any other deck
- Turns: 12
- Auditor variation: Not allowed

---

## Turn 1

### Enter

```text
make a quiz using the same sources as before
```

### Expect

- Recognises this is a fresh chat with no prior sources and does **NOT** invent or claim "the same
  sources".
- Asks which deck to use, or states that nothing is currently selected (a false source claim = Critical fail).

### Record

- Actual prompt entered:
- Files selected:
- Files Fazah used:
- Result: Pass / Small Issue / Fail / Critical Fail
- Short note:

---

## Turn 2  (continue the same chat — select `php_loops_presentation.pptx`)

### Enter

```text
use this one
```

### Expect

- Grounds in the now-selected `php_loops` deck (while / do…while / for / foreach).
- Asks how many questions or proceeds; no facts outside php_loops.

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
make a 5 q quiz on loops
```

### Expect

- Exactly five questions covering the four loops, grounded in php_loops.
- No answers shown yet; no new topics introduced.

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
add the answers
```

### Expect

- One correct answer per question, each supported by php_loops (e.g. do…while always runs at least once).
- Still exactly five questions.

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
now a student version, no answers
```

### Expect

- The same five questions in a student-facing version with NO answers shown
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
which source did u use, just to be sure
```

### Expect

- Names `php_loops_presentation.pptx` as the only source used.
- Confirms no earlier or "same as before" source was used — only the deck selected in this chat.

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
add a trace-the-output q, so 6
```

### Expect

- Adds one trace-the-output question grounded in php_loops (e.g. a do…while starting at 6 with `i<=5`
  prints 6, or `while $i<=5` prints `1 2 3 4 5`).
- Count is now six; earlier questions preserved.

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
teacher key w short explanations
```

### Expect

- A teacher key with the correct answer + a short explanation for each of the six, grounded in php_loops.
- The student version stays answer-free.

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
make 2 harder
```

### Expect

- Exactly two questions become harder; the other four are preserved. Still six, still grounded.

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
reorder easiest to hardest
```

### Expect

- The same six questions reordered easiest → hardest; none added or dropped, content unchanged.

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
verify its 6 n all from the loops deck
```

### Expect

- Confirms exactly six questions, all grounded in php_loops.
- Reaffirms the single source and that no other/"before" source was pulled in.

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
inventory of what we built
```

### Expect

- Lists what was made: a 6-question loops quiz, a student version (no answers), and a teacher key.
- Names the single source: `php_loops_presentation.pptx`.

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
