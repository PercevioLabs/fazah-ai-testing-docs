# S032 — Cursor teaching slide deck

## Tests

From the explicit-cursor lecture, Fazah builds an 8-slide teaching deck and then handles a run of
slide-specific edits — simplify one slide, convert one to a table, add a code scenario, add speaker
notes without touching slide text, insert a title and agenda slide, turn the last into a summary —
before deriving a student handout, all grounded in the one selected file.

## Setup

- Start: New chat
- Select files: `Lec5.pdf` (explicit cursors)
- Do not select: any other lecture
- Turns: 10
- Auditor variation: Allowed — see below (change exactly one instruction)

---

## Turn 1

### Enter

```text
make an 8 slide teaching deck on explicit cursors
```

### Expect

- An 8-slide teaching deck on explicit cursors, grounded in Lec5 (four-step lifecycle
  `DECLARE`→`OPEN`→`FETCH`→`CLOSE`, `%FOUND`/`%NOTFOUND`/`%ROWCOUNT`, fetch loop styles).
- Exactly 8 slides; content matches Lec5's employees example — no fabricated attributes or columns.
- Grounded in `Lec5.pdf`; no unselected-lecture citation.

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
make slide 2 simpler
```

### Expect

- New version: only slide 2 is simplified; slides 1 and 3–8 are unchanged.
- Still 8 slides, still grounded in Lec5.

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
turn slide 4 into a comparison table of the fetch loop styles
```

### Expect

- Slide 4 becomes a comparison table of the fetch loop styles (simple `LOOP` + `EXIT WHEN
  emp_cur%NOTFOUND` vs `WHILE emp_cur%FOUND LOOP` vs cursor `FOR` loop) — per Lec5.
- Only slide 4 changes; the other slides are preserved; still 8 slides.
- No invented loop style; table content is grounded in Lec5.

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
add a code scenario to slide 6
```

### Expect

- A code scenario is added to slide 6 in Lec5 style (`DECLARE`/`OPEN`/`FETCH ... INTO`/`CLOSE` over
  `employees`).
- Only slide 6 changes; the other slides are preserved.
- Code is grounded — deck columns (`employee_id`, `last_name`, `salary`), no fabrication.

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
add speaker notes but dont change the slide text
```

### Expect

- Speaker notes are added; the visible slide text is unchanged on every slide (edits leaking into
  slide bodies = fail).
- Notes are grounded in Lec5.

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
add a title slide
```

### Expect

- A title slide is added (the deck now has the 8 content slides plus a title slide); existing slides
  are preserved in order.
- Still grounded in Lec5.

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
add an agenda slide too
```

### Expect

- An agenda slide is added; the prior slides (title + 8 content) are preserved.
- The agenda lists the deck's actual explicit-cursor topics; grounded in Lec5.

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
make the last slide a summary
```

### Expect

- The last slide becomes a summary of the explicit-cursor material; only that slide changes.
- The summary is accurate to Lec5; the other slides are untouched.

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
make a student handout from the deck
```

### Expect

- A student handout derived from the deck (student-facing summary of explicit cursors), grounded in
  Lec5.
- The teacher-only speaker notes are NOT carried into the student handout; the deck is preserved.

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
which file did u use
```

### Expect

- Names `Lec5.pdf` (explicit cursors) as the source used throughout.
- Does not claim the implicit-cursor lecture (`Lec5_1.pdf`) or any unselected file.

### Record

- Actual prompt entered:
- Files selected:
- Files Fazah used:
- Result: Pass / Small Issue / Fail / Critical Fail
- Short note:

---

## Auditor variation

You may change **exactly one** instruction in one turn (keep every other prompt verbatim). Pick one,
and record what you changed and how Fazah adapted — the count/constraint in the affected Expect line
moves with your change:

- Turn 1: change the slide count ("make a 6 slide deck" / "make it 12 slides") — expect exactly that
  many slides.
- Turn 1: change the audience ("for first-year students") — simpler wording, still grounded in Lec5.
- Turn 1: add a title slide up front ("start with a title slide") — expect a title slide plus the 8
  content slides.
- Turn 1: make slide 1 an agenda ("make the first slide an agenda") — expect an agenda opener listing
  the cursor topics.

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
