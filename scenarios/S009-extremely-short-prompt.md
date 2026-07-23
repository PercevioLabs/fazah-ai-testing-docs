# S009 — Extremely short prompt

## Tests

Fazah recognizes the intended concept from a minimal two-word prompt and sustains a terse,
rushed teacher's follow-ups on the same waterfall topic without over-clarifying or losing context.

## Setup

- Start: New chat
- Select files: none
- Do not select: n/a
- Turns: 6
- Auditor variation: Not allowed

---

## Turn 1

### Enter

```text
explain waterfall
```

### Expect

- Recognizes the intent as the waterfall model (Software Processes, Ch2) — not something unrelated.
- Describes it as plan-driven with sequential/distinct phases.
- Proceeds rather than over-clarifying a clear request.

### Record

- Actual prompt entered:
- Files selected:
- Files Fazah used:
- Result: Pass / Small Issue / Fail / Critical Fail
- Short note:

---

## Turn 2   (continue the same chat)

### Enter

```text
list the phases
```

### Expect

- Lists the five phases: requirements analysis & definition → system & software design →
  implementation & unit testing → integration & system testing → operation & maintenance.
- Stays on the same waterfall model from turn 1 (does not restart or switch topic).

### Record

- Actual prompt entered:
- Files selected:
- Files Fazah used:
- Result: Pass / Small Issue / Fail / Critical Fail
- Short note:

---

## Turn 3   (continue the same chat)

### Enter

```text
main drawback?
```

### Expect

- Names the main drawback: hard to accommodate change once the process is underway.
- Answer is understood as being about waterfall (resolves the terse follow-up from context).

### Record

- Actual prompt entered:
- Files selected:
- Files Fazah used:
- Result: Pass / Small Issue / Fail / Critical Fail
- Short note:

---

## Turn 4   (continue the same chat)

### Enter

```text
when is it a good fit?
```

### Expect

- States waterfall suits stable, well-understood requirements and large systems-engineering projects.
- Consistent with the earlier drawback (fits when requirements are unlikely to change).

### Record

- Actual prompt entered:
- Files selected:
- Files Fazah used:
- Result: Pass / Small Issue / Fail / Critical Fail
- Short note:

---

## Turn 5   (continue the same chat)

### Enter

```text
make 3 quick questions
```

### Expect

- Produces exactly three short questions about waterfall (phases, drawback, or good fit).
- Questions draw only on what was covered above — no new unrelated process models introduced.

### Record

- Actual prompt entered:
- Files selected:
- Files Fazah used:
- Result: Pass / Small Issue / Fail / Critical Fail
- Short note:

---

## Turn 6   (continue the same chat)

### Enter

```text
which file?
```

### Expect

- Points to the Software Processes deck (`Ch2 SW Processes.pptx`) as where waterfall is covered.
- Does not invent a different or non-existent source.

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

For the complete workflow, see [Context Diagram](../CONTEXT-DIAGRAM.md).
