# S032 — Operators 8-slide deck, long iterative build

## Tests

With only the operators deck selected, Fazah builds an 8-slide teaching deck on PHP operators, then
sustains a 20-turn iterative build — per-slide edits, a `==` vs `===` comparison table, speaker notes,
title/agenda/recap/summary slides, a power-operator slide, a student handout, and numbering/slide-count
verification — all grounded in the same deck (which carries a "(2)" version tag) and answer-free where
student-facing.

## Setup

- Start: New chat
- Select files: `php_operators_presentation (2).pptx`
- Do not select: any other deck
- Turns: 20
- Auditor variation: Allowed (see Auditor variation section below)

---

## Turn 1

### Enter

```text
make an 8 slide teaching deck on operators
```

### Expect

- Produces an 8-slide teaching deck on PHP operators (arithmetic `+ - * / % **`, assignment, comparison, etc.).
- Grounded in `php_operators_presentation (2).pptx`; no other deck.

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
slide 2 is too complex, make it simpler
```

### Expect

- Simplifies slide 2 only; the other slides are unchanged.
- Still 8 slides, still grounded.

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
turn slide 4 into a comparison table, == vs ===
```

### Expect

- Slide 4 becomes a comparison table contrasting `==` (equal value) vs `===` (equal value and type).
- Accurate to the deck; other slides unchanged.

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

- Adds a short, valid-PHP code scenario to slide 6 (e.g. arithmetic or assignment operators).
- Consistent with the deck; other slides untouched.

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

- Adds speaker notes to the slides while leaving the visible slide text unchanged.
- Notes grounded in operator facts.

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
add a title slide at the front
```

### Expect

- Adds a title slide at the front; slide count increases and numbering shifts accordingly.
- Existing content is preserved.

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
add an agenda slide after the title
```

### Expect

- Adds an agenda/overview slide after the title.
- Prior slides preserved; numbering consistent.

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

- The last slide becomes a summary of the operator categories covered.
- Accurate; other slides unchanged.

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

- Produces a student handout derived from the deck content.
- Grounded; if any embedded questions, no answers are shown (answer-leakage check — leaked answers = Critical fail).

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
which deck did u pull from
```

### Expect

- Names `php_operators_presentation (2).pptx` (the operators deck, including its "(2)" tag) as the source.
- Does not invent a different operators file; no unselected deck claimed.

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
add a slide on the ** power operator
```

### Expect

- Adds a slide on the `**` power operator (e.g. `10 ** 3` = 1000), grounded in the deck.
- Slide count updated; other slides preserved.

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
did the slide numbering stay correct after all the edits
```

### Expect

- Confirms slide numbering is sequential/consistent after the insertions.
- Fixes any gaps without changing content.

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
make slide 3 a worked example
```

### Expect

- Slide 3 becomes a step-by-step worked example grounded in an operator (e.g. `%` modulus or arithmetic).
- Valid PHP; other slides unchanged.

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
add != and !== to that comparison table too
```

### Expect

- The comparison table (slide 4) also shows `!=` (not equal value) and `!==` (not equal value or type) accurately.
- No slide-count change; other content preserved.

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
add a recap slide near the end
```

### Expect

- Adds a recap slide before the summary.
- Prior slides preserved; numbering consistent.

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
add a slide on assignment operators, += -= etc
```

### Expect

- Adds a slide on assignment operators (`= += -= *= /= %=`), grounded in the deck.
- Slide count updated; other slides preserved.

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
the speaker notes are too long, shorten them
```

### Expect

- Shortens the speaker notes while leaving the slide text unchanged.
- Notes stay accurate.

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
how many slides now
```

### Expect

- Reports the current slide count accurately (8 core + title + agenda + power + recap + assignment additions).
- The number is consistent with the edits made.

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
if any slides have questions make a student version w/ no answers
```

### Expect

- Provides a student version of any embedded questions with NO answers
  (answer-leakage check — leaked answers = Critical fail).
- If there are no embedded questions, says so honestly rather than inventing any.

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
give me the full inventory
```

### Expect

- Inventory: the full slide deck (with title, agenda, recap, summary, power, assignment slides),
  speaker notes, student handout, and student question version.
- Matches produced content; no invented items.

### Record

- Actual prompt entered:
- Files selected:
- Files Fazah used:
- Result: Pass / Small Issue / Fail / Critical Fail
- Short note:

---

## Auditor variation

Optional swaps an auditor may substitute for a single turn without breaking the grounding or the
answer-free rule (keep all other turns as written):

- Change the starting slide count (e.g. 6 slides or 10 slides) instead of 8 — Fazah must keep numbering consistent.
- Change the audience (e.g. first-year students) — content stays grounded in the operators deck.
- Ask for the title slide as the very first turn rather than mid-arc.
- Make slide 1 the agenda instead of adding a separate agenda slide.

Any student-facing asset (handout, embedded-question version) must remain answer-free regardless of the variation chosen.

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
