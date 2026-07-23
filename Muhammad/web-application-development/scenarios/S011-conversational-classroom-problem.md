# S011 — Conversational classroom problem, no file selected

## Tests

A teacher opens with a real classroom pain point (single vs double quotes) in a chatty, casual voice
and nothing selected. Fazah must recognise the strings material, ground everything in the strings deck
without being told, and build a small teach-then-check kit — opening activity, examples, handout, exit
ticket, student/teacher split — while naming the source correctly mid-conversation.

## Setup

- Start: New chat
- Select files: none (start with nothing selected)
- Do not select: leave everything unselected — Fazah must find the right deck itself
- Turns: 14
- Auditor variation: Not allowed

---

## Turn 1

### Enter

```text
ok so my students keep mixing up single vs double quotes, can u help me explain it before class
```

### Expect

- Explains single quotes are literal (no variable parsing) and double quotes parse variables/escapes —
  e.g. `echo 'Hello $name'` prints `Hello $name`, `echo "Hello $name"` prints the value.
- With no file selected, grounds the answer in the strings deck (php_strings) rather than guessing.
- No invented citation to a deck that was never selected.

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
gimme a quick 2 min opening activity to kick it off
```

### Expect

- A short (~2 min) opening activity that surfaces the single vs double quote difference.
- Stays grounded in php_strings; no new topics introduced.

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
add like 3 quick examples showing the difference
```

### Expect

- Exactly 3 short valid PHP examples contrasting `'...'` and `"..."` output with a variable.
- Consistent with the deck's own examples; no fabricated behaviour.

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
can u make a short handout from that
```

### Expect

- A concise student handout built from the explanation + 3 examples.
- Grounded content only; no answers to any later quiz baked in.

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
ok now a 3 question exit ticket
```

### Expect

- Exactly 3 exit-ticket questions on single vs double quotes, grounded in php_strings.
- Each has a defensible correct answer for the teacher.

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
student version pls, no answers on it
```

### Expect

- The same 3 exit-ticket questions with NO answers shown
  (answer-leakage check — leaked answers = Critical fail).

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
oh can u add a strpos example too
```

### Expect

- Adds a valid `strpos()` example: 0-indexed position, e.g. `strpos("Hello world!", "world")` returns 6,
  and returns FALSE if not found.
- Consistent with php_strings; does not silently drop earlier content.

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
which lecture is this from btw
```

### Expect

- Names the strings deck (`php_strings_presentation.pptx`) as the source, even though it was never manually selected.
- Does not claim a different or unselected deck, and does not say it had no source.

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
actually make those exit ticket qs a bit harder
```

### Expect

- The 3 exit-ticket questions become harder (e.g. predict-the-output, strpos edge cases); still 3.
- Still grounded in php_strings.

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
and gimme the teacher key w the answers
```

### Expect

- A teacher key with the correct answer + short explanation for each of the 3 questions.
- The student version from Turn 6 stays answer-free.

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
can u shorten the handout to like half a page
```

### Expect

- Trims the handout to roughly half a page while keeping the core single vs double quote point.
- Does not lose the examples entirely or drift off php_strings.

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
add one more example showing the . concatenation
```

### Expect

- Adds a valid example using the `.` concatenation operator to join strings.
- Grounded in php_strings (concatenation with the `.` operator).

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
ok redo the student version and double check no answers are in it
```

### Expect

- Re-issues the student exit ticket with NO answers or explanations exposed
  (answer-leakage check — leaked answers = Critical fail).

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
cool, give me a final list of everything we made
```

### Expect

- A clear inventory: opening activity, examples (incl. strpos and concatenation), handout, exit ticket
  (student + teacher versions).
- Counts and pieces match what was actually produced; nothing invented.

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
