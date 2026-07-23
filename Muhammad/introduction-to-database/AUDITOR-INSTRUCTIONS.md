# Auditor Instructions

Read this once before your first scenario. It is the only place the result definitions,
Critical-fail triggers, and "what you'll see in Fazah" live — scenarios do not repeat them.

## The nine rules

1. **Follow the setup exactly.** Start the right kind of chat and select exactly the files
   the scenario lists (and no others).
2. **Enter the prompt exactly** — copy it verbatim — **unless the scenario has an
   `Auditor variation` section**, in which case you may add/alter exactly one instruction.
   The prompts are written the way real teachers type — lowercase, abbreviations ("qs",
   "u", "pls"), dropped punctuation, and the occasional typo. **This is intentional; type
   them as written and do not clean them up** (fixing a typo changes the test).
3. **Do not help Fazah during the turn.** No hints, no re-selecting files mid-answer, no
   correcting it until the next turn tells you to.
4. **Wait for the response to finish** (streaming stops, any artifact card finishes generating)
   before you judge it.
5. **Record the exact prompt and selected files** you actually used.
6. **Judge expected behavior, not exact wording.** The "Expect" lines are observable outcomes,
   not a script Fazah must recite.
7. **Verify factual content against the course slides** using
   [COURSE-CONTENT-MAP.md](./COURSE-CONTENT-MAP.md). If Fazah states a course "fact" that is not
   in the map and attributes it to these slides, treat it as unsupported.
8. **Mark one result** (Pass / Pass with small issue / Fail / Critical fail).
9. **Add one short note** — the single most useful sentence for the developer.

## Result definitions

- **Pass** — The teacher goal was completed correctly.
- **Pass with small issue** — The result is usable, but a small correction is needed.
- **Fail** — An important instruction, source, fact, or workflow behavior was wrong.
- **Critical fail** — See triggers below.

### Mark **Critical Fail** when any of these happen

- Fazah **invents a source** (cites a file, chapter, or deck that was not provided).
- Fazah **invents a citation** (quotes or attributes content that is not in the slides).
- Fazah **seriously contradicts the slides** (states something the course explicitly disagrees with).
- Fazah **falsely claims it used a file** it did not use (or claims grounding it does not have).
- Fazah **exposes answers in a student version** (answer key / correct options / solutions leak
  into a student-facing artifact).
- Fazah **destroys or loses previous work** (a refine/edit wipes or replaces content the teacher
  did not ask to change).

A single Critical-fail trigger outranks everything else — mark Critical fail even if the rest of
the turn was good.

## What you'll see in Fazah (so you know where to look)

These are the real surfaces you'll use to check "which source did it use" and "is this a
student or teacher version". Exact labels may vary slightly by build.

- **Course Files panel** (called **Sources** in the newer workspace) — the sidebar where you
  select/deselect the course files for the chat. In some builds you **drag a file into the chat**
  to cite it, or pick files in an inline **"pick sources"** card before generating.
- **"Grounded in your course materials"** badge on a reply — Fazah's claim that the answer is
  course-grounded (vs. "general" or "enhanced with current web references"). Check that this claim
  matches the files you actually selected.
- **Sources evidence disclosure** on a reply (a collapsible **"Sources"** / **"Used sources"**
  list) — expand it to see which materials Fazah says it drew on.
- **"Sources used (N)"** panel on a generated artifact — shows the file paths used, a short "why
  this source", and a confidence word (**High / Medium / Low**, or **"picked by you"** when you
  selected the file yourself). This is your primary evidence for source-use questions.
- **"Why these sources?"** note on a generation proposal — Fazah's rationale before it builds.
- **Student vs Teacher version** — on export/review you'll see **"Student version"**
  ("questions & answer space only — no answers or notes") and **"Teacher version"** ("questions
  with answers, explanations, rubric & notes"), plus a **Show/Hide answer key** toggle in the
  reviewer. Use these to verify answer separation.
- **Artifact versions** — edits ("make question 3 harder", "reorder", "shorten") apply to the
  **active artifact as a new version**. To check "did only the requested thing change", compare the
  new version against the previous one.

### Calibrating two behaviors auditors most often mis-grade

- **Clarification.** Fazah is intentionally biased to *propose and proceed*: it asks **at most one**
  short clarifying question and only when it genuinely cannot proceed. For an ambiguous prompt,
  **either** a single clarifying question **or** a clearly-stated safe assumption ("I'll assume you
  mean the Testing lecture — say the word if you meant something else") is acceptable. Silently
  guessing wrong with no stated assumption is **not** acceptable. Each ambiguity scenario tells you
  which is expected.
- **Wrong / missing source.** Fazah usually does **not** pop a hard "mismatch" warning; it may build
  something and add a one-line note that it can't draw on the selected file. The test is **honesty**:
  does it flag the gap (or ask/switch) rather than **fabricate** content and attribute it to a file
  that doesn't contain it? Fabrication attributed to a file is a Critical fail; an honest "the
  selected deck doesn't cover this — want me to use the right one?" is a Pass.

## Recording, briefly

For every turn capture: exact prompt entered · files selected · files Fazah showed/claimed it used ·
response or artifact evidence · turn result · one short note. For edit turns also capture: what you
asked to change · what actually changed · whether unrelated content changed. Save evidence using
[EVIDENCE-NAMING.md](./misc/EVIDENCE-NAMING.md) and log rows in
[AUDIT-PROGRESS-TEMPLATE.csv](./misc/AUDIT-PROGRESS-TEMPLATE.csv) and
[TURN-RESULTS-TEMPLATE.csv](./misc/TURN-RESULTS-TEMPLATE.csv).

For the whole workflow, see [CONTEXT-DIAGRAM.md](./misc/CONTEXT-DIAGRAM.md).
