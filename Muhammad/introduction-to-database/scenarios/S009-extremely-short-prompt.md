# S009 — Extremely short prompts, no file selected

## Tests

With no lecture selected, Fazah handles a run of terse one-line prompts about the FOR loop, keeps the
thread across follow-ups, answers only at loops-lecture depth, and is honest that no file was the
source.

## Setup

- Start: New chat
- Select files: none
- Do not select: any lecture (the FOR loop is loops-lecture content — Lec3 — but nothing is selected)
- Turns: 6
- Auditor variation: Not allowed

---

## Turn 1

### Enter

```text
explain for loop
```

### Expect

- Explains the PL/SQL FOR loop: iterates over a range, e.g. `FOR i IN 1..5 LOOP ... END LOOP;` —
  consistent with Lec3.
- No file is selected, so Fazah answers generally or notes nothing is selected; it does NOT invent a
  citation to a lecture it was not given.
- Stays at loop-basics depth; no fabricated deck facts.

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
syntax?
```

### Expect

- Understands "syntax?" refers to the FOR loop from Turn 1 (does not restart on a new topic).
- Gives `FOR i IN 1..5 LOOP ... END LOOP;` — matching Lec3.
- No fabricated citation.

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
whats reverse do
```

### Expect

- Explains `REVERSE` counts down: `FOR i IN REVERSE 1..5 LOOP ...` iterates from high to low — per Lec3.
- Still on the FOR loop thread.
- No fabricated behavior beyond the deck.

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
when do i use it
```

### Expect

- Explains when a FOR loop fits: a known/fixed number of iterations over a range, versus while / simple
  loop — consistent with Lec3's three-loop framing.
- Does not drift outside loops.

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
make 3 quick qs
```

### Expect

- Exactly 3 short questions on the FOR loop / reverse material discussed above — not new topics.
- Questions answerable at Lec3 loop level; MCQ or trace-the-output both acceptable.
- No fabricated loop constructs.

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
which lecture?
```

### Expect

- Honest about source: no lecture was selected, so it should say nothing was selected (this maps to the
  loops lecture but was not grounded in a selected file).
- Does NOT claim it used `Lec3.pdf` or any specific file when none was selected.

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
