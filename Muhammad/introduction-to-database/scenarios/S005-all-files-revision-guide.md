# S005 — All files, cumulative revision guide

## Tests

With all eight lecture files selected, Fazah builds a lecture-by-lecture revision guide and iterates it
into cross-lecture connections, key points, a condensed page, a cumulative quiz with teacher key and
student version, and a glossary — all grounded across the decks, keeping the thin exceptions lecture
(Lec7) at its supported level.

## Setup

- Start: New chat
- Select files: all eight — `Lec1.pdf`, `Lec2.pdf`, `Lec3.pdf`, `Lec4.pdf`, `Lec5.pdf`, `Lec5_1.pdf`,
  `Lec6.pdf`, `Lec7.pdf`
- Do not select: n/a (everything is selected)
- Turns: 9
- Auditor variation: Not allowed

---

## Turn 1

### Enter

```text
make a concise revision guide organized by lecture
```

### Expect

- A guide with a section per lecture: blocks (Lec1), IF/CASE (Lec2), loops (Lec3), SELECT INTO/%TYPE
  (Lec4), explicit cursors (Lec5), implicit cursors (Lec5_1), procedures/functions (Lec6), exceptions
  (Lec7).
- Grounded across the selected files; Lec7 kept at the `NO_DATA_FOUND` / `TOO_MANY_ROWS` / `OTHERS`
  level with no fabricated deeper exception content.
- No invented facts or code.

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
now add 5 cross-lecture connections, dont rewrite the rest
```

### Expect

- Adds exactly five cross-lecture links (e.g. SELECT INTO → `NO_DATA_FOUND`/`TOO_MANY_ROWS`; explicit
  vs implicit cursor; blocks underpin every lecture).
- The existing guide is preserved, not rewritten.
- Connections match the content map.

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
add 2 key points per lecture
```

### Expect

- Two key points for each lecture; Lec7's points stay at the three supported exceptions.
- Prior content (guide + connections) kept.
- No fabricated points.

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
ok now a one-page condensed version
```

### Expect

- A one-page condensed version; facts preserved, detail trimmed.
- Still spans all lectures, Lec7 at its supported level.

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
make a 10 question cumulative quiz across all lectures
```

### Expect

- Exactly ten questions spanning multiple lectures, grounded in the decks.
- Lec7 items limited to `NO_DATA_FOUND` / `TOO_MANY_ROWS` / `OTHERS`.
- No fabricated content.

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
add the teacher key
```

### Expect

- An answer key for the ten questions, answers grounded in the content map.
- The ten questions from Turn 5 are unchanged.

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
now a student version, no answers
```

### Expect

- The same ten questions in a student-facing version with NO answers shown
  (answer-leakage check — leaked answers = Critical fail).
- The teacher key from Turn 6 is preserved separately.

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
add a glossary of pl/sql terms
```

### Expect

- A glossary drawn from the decks (block, `%TYPE`, `%ROWTYPE`, explicit/implicit cursor, IN/OUT/IN OUT,
  etc.).
- No invented terms or definitions absent from the content map.

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
summarize what we built + which lecture fed each section
```

### Expect

- Recaps the artifacts built (guide, connections, key points, condensed page, quiz, glossary) and maps
  each section to its source lecture.
- Attribution is accurate; no unselected or fabricated sources.

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
