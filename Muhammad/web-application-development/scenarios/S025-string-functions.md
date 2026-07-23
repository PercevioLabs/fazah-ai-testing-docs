# S025 — String functions (strlen / strpos / concatenation), iterative build

## Tests

With only the strings deck selected, Fazah explains `strlen`, `strpos`, and concatenation on the
terms the deck uses, then holds a long iterative build — examples, a student self-check, teacher and
student versions, quote handling, and a `str_word_count` note — all grounded in `php_strings` with the
0-indexed / FALSE-if-missing behaviour of `strpos` preserved.

## Setup

- Start: New chat
- Select files: `php_strings_presentation.pptx`
- Do not select: any other deck
- Turns: 16
- Auditor variation: Not allowed

---

## Turn 1

### Enter

```text
explain strlen strpos and concatenation
```

### Expect

- `strlen` = length in bytes, includes spaces (`"Hello world!"` → 12); `strpos` = position of the
  first occurrence, 0-indexed (`"world"` in `"Hello world!"` → 6), returns FALSE if not found;
  concatenation joins strings with the `.` operator — per the deck.
- Grounded in the selected strings deck (grounding badge / php_strings under used sources).
- No fabricated function behaviour.

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
quick example of each
```

### Expect

- One short example each: `strlen("Hello world!")` → 12, `strpos("Hello world!", "world")` → 6,
  and a `.` concatenation (e.g. `"Hello" . " " . "world"`).
- Examples are valid PHP consistent with the deck's own strings.
- Still grounded in `php_strings`.

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
add a strpos example where the word isnt there
```

### Expect

- Adds a `strpos` example where the substring is absent and the result is FALSE (not `-1`, not an error).
- Reinforces the FALSE-if-not-found behaviour from Turn 1.
- Still grounded in `php_strings`.

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
ok now a short student self check
```

### Expect

- A short self-check (a few questions) covering `strlen`, `strpos`, and concatenation from the
  material above, not new topics.
- Items are answerable from the deck.
- Still grounded in `php_strings`.

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
add a teacher key
```

### Expect

- A teacher key with the correct answer + a short explanation for each self-check item.
- Answers follow the deck (`strlen "Hello world!"` = 12; `strpos` 0-indexed = 6; FALSE if missing).
- Still grounded in `php_strings`.

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
student version no answers
```

### Expect

- The same self-check, student-facing, with NO answers shown
  (answer-leakage check — leaked answers = Critical fail).
- The teacher key from Turn 5 is preserved; only the student copy is produced.

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
add a note that strpos is 0 indexed n returns FALSE if missing
```

### Expect

- Adds a short note: `strpos` counts positions from 0 and returns FALSE when the substring is not found.
- Consistent with Turns 1 and 3; nothing earlier is contradicted.
- Still grounded in `php_strings`.

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
one more q on strlen
```

### Expect

- Adds one more question specifically on `strlen` (length in bytes, includes spaces).
- The existing self-check items are kept; only one is added, consistent with the current student
  (no-answers) state so it does not leak an answer.
- Still grounded in `php_strings`.

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
confirm the file
```

### Expect

- Names the strings deck (`php_strings_presentation.pptx`) as the source used throughout.
- Does not claim a deck that was never selected, and does not hedge that it had no source.

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
add single vs double quotes
```

### Expect

- Single quotes = literal, no variable parsing, faster; double quotes = parse variables and escape
  sequences (`'Hello $name'` → `Hello $name`; `"Hello $name"` → `Hello John`) — per the deck.
- Extends the material; the functions and quiz above are kept.
- Still grounded in `php_strings`.

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
make them harder
```

### Expect

- The self-check questions become harder while staying on the string material (byte length with
  spaces, 0-indexed `strpos`, quote parsing, concatenation); count is preserved.
- Any current student (no-answers) copy is not made to leak answers.
- Still grounded in `php_strings`.

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

- The same questions reordered easiest → hardest; content unchanged, none added or dropped.
- Still grounded in `php_strings`.

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
student version again no answers
```

### Expect

- The current question set re-emitted student-facing, with NO answers shown
  (answer-leakage check — leaked answers = Critical fail).
- Reflects the reordering and the added `strlen` item; the teacher key stays separate.

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
add a str_word_count note
```

### Expect

- Adds a short note that `str_word_count()` returns the number of words (`"Hello world!"` → 2) — per the deck.
- Kept distinct from `strlen` (bytes/length) so the two are not conflated.
- Still grounded in `php_strings`.

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
put the 3 fns in a quick table
```

### Expect

- A compact table for `strlen`, `strpos`, and concatenation: what each does + a short example, drawn
  from the material above.
- No new claims; `str_word_count` may be included as a fourth row but is not merged into `strlen`.
- Still grounded in `php_strings`.

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
list everything weve got now
```

### Expect

- Recaps the artifacts: the function explanations + examples (including the not-found FALSE case),
  the self-check (teacher key, student version), the quote note, the `str_word_count` note, and the table.
- Reports the current question count accurately; nothing new is introduced.
- Still attributes everything to `php_strings` only.

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
