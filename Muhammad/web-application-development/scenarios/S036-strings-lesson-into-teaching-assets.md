# S036 — Strings lesson transformed into teaching assets

## Tests

From one selected deck (php_strings), Fazah builds a 50-minute lesson and then, across 24 iterative
turns, spins it into a connected set of teaching assets — handout, exit ticket, slides, glossary,
homework, revision sheet — keeping every asset grounded in the same source, splitting student-facing
material from teacher answers, and reporting an accurate inventory without answer leakage.

## Setup

- Start: New chat
- Select files: `php_strings_presentation.pptx`
- Do not select: any other deck
- Turns: 24
- Auditor variation: Not allowed

---

## Turn 1

### Enter

```text
make a 50 min lesson on strings — quotes, strlen, strpos, concatenation
```

### Expect

- A 50-minute lesson plan covering single vs double quotes, `strlen`, `strpos`, and `.` concatenation.
- Facts match php_strings (e.g. `strlen("Hello world!")` → 12; `strpos` 0-indexed, FALSE if missing).
- Grounded in the selected strings deck; no unselected deck cited.

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
shorten the teacher explanation part to 15 min
```

### Expect

- Only the explanation segment is cut to ~15 min; the rest of the 50-min plan is preserved and still adds up.

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
add a pair coding activity
```

### Expect

- A paired coding activity added, grounded in string operations from the deck (e.g. build/measure a string).
- Existing lesson sections retained.

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
add a trace-the-output scenario
```

### Expect

- A trace-the-output item with valid PHP (e.g. `echo 'Hello $name'` → `Hello $name` vs `echo "Hello $name"` parses).
- Consistent with the single vs double quote behavior in php_strings.

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
now a one-page student handout
```

### Expect

- A one-page student-facing handout summarizing the string concepts (no teacher-only notes or answers).
- Grounded in php_strings (answer-leakage check — leaked answers = Critical fail).

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
5 exit-ticket questions
```

### Expect

- Exactly 5 exit-ticket questions on the lesson's string topics, answerable from the deck.

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
put the exit ticket answers in a separate teacher sheet
```

### Expect

- A separate teacher answer sheet for the 5 exit-ticket questions.
- The exit ticket itself stays answer-free.

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
add learning objectives
```

### Expect

- Clear learning objectives added to the lesson, matching the covered string concepts.
- No change to the handout or exit ticket content.

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
make a 4-slide recap
```

### Expect

- A 4-slide recap of the string material (quotes, strlen, strpos, concatenation), grounded in php_strings.

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
and a student revision sheet
```

### Expect

- A student-facing revision sheet summarizing the topics with no answers to the exit ticket
  (answer-leakage check — leaked answers = Critical fail).

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
summarize all the assets + confirm same source
```

### Expect

- Lists the assets built so far (lesson, activity, handout, exit ticket, teacher sheet, objectives, recap, revision sheet).
- Confirms all came from `php_strings_presentation.pptx`; no false claim of another deck (Critical fail if it does).

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
double check the student handout has no answers
```

### Expect

- Confirms the student handout contains no answers or teacher notes
  (answer-leakage check — any leak = Critical fail).

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
add a strpos activity
```

### Expect

- An activity practising `strpos` (0-indexed position; returns FALSE if not found), grounded in the deck.
- Prior assets preserved.

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
add a glossary of the string terms
```

### Expect

- A glossary defining the string terms used (quotes, strlen, strpos, concatenation) consistent with php_strings.

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
shorten the handout to half a page
```

### Expect

- Only the student handout is trimmed to ~half a page; other assets untouched.
- Still student-facing, still no answers.

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
add a note on single vs double quotes
```

### Expect

- A note added contrasting single quotes (literal, no variable parsing) and double quotes (parse variables).
- Matches php_strings (`'Hello $name'` literal vs `"Hello $name"` parsed).

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
verify each asset is still there
```

### Expect

- Confirms all assets still exist (lesson, activities, handout, exit ticket, teacher sheet, objectives, recap, revision sheet, glossary, note).

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
add a homework task
```

### Expect

- A homework task grounded in the string concepts (e.g. write a script using strlen/strpos/concatenation).

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
add short explanations to the exit ticket teacher key
```

### Expect

- Each exit-ticket answer in the teacher sheet gains a short explanation grounded in php_strings.
- The student-facing exit ticket stays answer-free.

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
re-check the student stuff — handout and revision sheet, no answers
```

### Expect

- Confirms both the handout and revision sheet are student-facing with no answers or teacher notes
  (answer-leakage check — any leak = Critical fail).

### Record

- Actual prompt entered:
- Files selected:
- Files Fazah used:
- Result: Pass / Small Issue / Fail / Critical Fail
- Short note:

---

## Turn 21  (continue the same chat)

### Enter

```text
label which assets are student facing vs teacher facing
```

### Expect

- Correctly labels each asset by audience (handout/revision sheet/exit ticket = student; teacher sheet/objectives/notes = teacher).
- No audience mix-up.

### Record

- Actual prompt entered:
- Files selected:
- Files Fazah used:
- Result: Pass / Small Issue / Fail / Critical Fail
- Short note:

---

## Turn 22  (continue the same chat)

### Enter

```text
add a concatenation example to the recap slides
```

### Expect

- A `.` concatenation example added to the 4-slide recap (e.g. `$a . " " . $b`), grounded in php_strings.
- Only the recap changes.

### Record

- Actual prompt entered:
- Files selected:
- Files Fazah used:
- Result: Pass / Small Issue / Fail / Critical Fail
- Short note:

---

## Turn 23  (continue the same chat)

### Enter

```text
final inventory of everything
```

### Expect

- Lists every asset with its audience; counts (e.g. 5 exit-ticket questions, 4 recap slides) match the running set.

### Record

- Actual prompt entered:
- Files selected:
- Files Fazah used:
- Result: Pass / Small Issue / Fail / Critical Fail
- Short note:

---

## Turn 24  (continue the same chat)

### Enter

```text
confirm the same strings deck fed all of it
```

### Expect

- Confirms `php_strings_presentation.pptx` as the single source for every asset.
- Does not claim any other deck (false source claim = Critical fail).

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
