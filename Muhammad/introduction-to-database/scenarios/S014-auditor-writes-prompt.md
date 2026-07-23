# S014 — Auditor writes the opening prompt, implicit cursors

## Tests

With the implicit-cursor lecture selected, the auditor writes their own opening prompt asking for a
beginner explanation of implicit cursors and the `SQL%` attributes; Fazah then carries it through an
analogy, a plain attribute list, beginner questions, and a student version — all grounded in Lec5_1.

## Setup

- Start: New chat
- Select files: `Lec5_1.pdf` (implicit cursors & SQL cursor attributes)
- Do not select: any other lecture (do not select `Lec5.pdf` — that is explicit cursors)
- Turns: 6
- Auditor variation: Allowed — see the Auditor variation section

---

## Turn 1

### Enter

Write your own opening prompt, in your own words, as a single natural chat message. Goal: ask Fazah to
explain implicit cursors and the `SQL%` cursor attributes for beginners. Record exactly what you typed.

### Expect

- Explains the implicit cursor (the `SQL` cursor, opened automatically by Oracle for `INSERT`,
  `UPDATE`, `DELETE`, and `SELECT INTO`) and the `SQL%` attributes for beginners — per Lec5_1.
- Grounded in `Lec5_1.pdf`; no fabricated depth beyond the deck; no invented citation.
- Beginner-appropriate framing.

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
add a simple analogy
```

### Expect

- Adds a plain analogy for the implicit cursor without changing the technical definition.
- The prior explanation is preserved.

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
list the SQL% attributes plainly (SQL%FOUND, SQL%NOTFOUND, SQL%ROWCOUNT)
```

### Expect

- Lists `SQL%FOUND` (TRUE if ≥1 row affected), `SQL%NOTFOUND` (TRUE if 0 rows), `SQL%ROWCOUNT` (number
  of rows affected) — per Lec5_1.
- Accurate and grounded; may also mention `SQL%ISOPEN` (always FALSE) but it is not required.

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
make 4 beginner qs
```

### Expect

- Exactly 4 beginner questions on implicit cursors / `SQL%` attributes.
- Answerable from Lec5_1; no fabricated content.

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
now a student version
```

### Expect

- A student-facing version of the 4 questions with NO answers shown
  (answer-leakage check — leaked answers = Critical fail).
- The teacher content is preserved.

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
which file did you use
```

### Expect

- Names `Lec5_1.pdf` (implicit cursors) as the source used.
- Does not claim the explicit-cursor lecture (`Lec5.pdf`) or any other unselected file.

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
- change the audience (e.g. high-school students)
- add "should take under a minute to read"
- ask for exactly one analogy
- request a more formal tone

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
