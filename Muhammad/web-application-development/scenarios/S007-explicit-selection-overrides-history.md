# S007 — Explicit selection overrides chat history

## Tests

The chat starts on the arrays deck, then the teacher explicitly selects the strings deck. Fazah should
let the new explicit selection override the earlier arrays history — grounding all subsequent answers
in the strings deck — and, when asked which file the questions came from, name the strings deck rather
than the arrays deck used earlier.

## Setup

- Start: New chat
- Select files: `php_arrays_presentation.pptx` (start); switched to `php_strings_presentation.pptx`
  at Turn 3
- Do not select: `php_strings_presentation.pptx` at the start
- Turns: 14
- Auditor variation: Not allowed

---

## Turn 1

### Enter

```text
explain indexed vs associative arrays
```

### Expect

- Indexed = numeric index starting at 0; associative = named keys (`"brand" => "Ford"`), matching the
  arrays deck.
- Grounded in `php_arrays_presentation.pptx`.

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
add multidimensional arrays to that
```

### Expect

- Multidimensional = arrays of arrays; consistent with the deck.
- Still grounded in the arrays deck.

### Record

- Actual prompt entered:
- Files selected:
- Files Fazah used:
- Result: Pass / Small Issue / Fail / Critical Fail
- Short note:

---

## Turn 3  (continue the same chat — now select php_strings and deselect php_arrays)

### Enter

```text
switched to the strings deck now. explain single vs double quotes
```

### Expect

- Single quotes = literal, no variable parsing, faster; double quotes = parse variables + escape
  sequences (`echo "Hello $name"` → `Hello John`), matching the strings deck.
- Explicit selection overrides history: grounded in `php_strings_presentation.pptx`, NOT the arrays deck.

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
keep using the strings file — what do strlen and strpos do
```

### Expect

- `strlen` = length in bytes (`"Hello world!"` → 12); `strpos` = position of first occurrence
  (0-indexed; `"world"` → 6; returns FALSE if not found), matching the deck.
- Still grounded in the strings deck.

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
gimme a code example using both
```

### Expect

- Short valid PHP using `strlen` and `strpos` on a string; consistent with the deck.
- No invented functions.

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
trace the output — strlen and strpos on 'Hello world!' looking for world
```

### Expect

- `strlen("Hello world!")` = 12; `strpos("Hello world!", "world")` = 6 — matching the deck's own
  example.
- Reasoning consistent with Turn 4.

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
make 5 qs from the strings file
```

### Expect

- Exactly 5 questions on strings (quotes, `strlen`, `strpos`, concatenation), each with a correct
  answer supported by the strings deck.

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
which file are these from
```

### Expect

- Names the strings deck (`php_strings_presentation.pptx`).
- Does NOT attribute them to the arrays deck used earlier in the chat.

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
reorder easiest to hardest
```

### Expect

- The same 5 questions reordered easiest → hardest; none added or dropped.

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
make 2 of them harder
```

### Expect

- Exactly two of the 5 become harder; the rest preserved.
- Still 5, still grounded in the strings deck.

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
student version, no answers
```

### Expect

- The same 5 questions, student-facing, with NO answers shown
  (answer-leakage check — leaked answers = Critical fail).

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
teacher key w explanations
```

### Expect

- Teacher key: correct answer + short explanation for each of the 5; the student version stays
  answer-free.

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
swap the weakest for a concatenation q
```

### Expect

- Replaces one question with a concatenation (`.` operator) question, grounded in the strings deck.
- Count stays at 5.

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
confirm all 5 are from strings and the arrays deck wasnt used after i switched
```

### Expect

- Confirms all 5 are grounded in the strings deck; the arrays deck was not used after the switch.
- Attribution accurate; explicit selection respected over history.

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
