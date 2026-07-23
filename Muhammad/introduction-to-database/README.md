# Fazah — Introduction to Database (Oracle PL/SQL) Manual Human-Audit Suite

**Prepared by: Muhammad**

A realistic, diverse suite of **40 multi-turn conversations** (6–16 turns each) that a human auditor
runs inside Fazah, using a real **Introduction to Database** course — which teaches **Oracle
PL/SQL** (Oracle's procedural extension to SQL). Every scenario is a sustained conversation on one
continuous teacher goal — no single-turn tests, because a real teacher rarely stops after one
message. The suite tests one question:

> **Can a real teacher complete a task in Fazah without repeatedly supervising or correcting it?**

Everything here is documentation, scenario design, audit templates, and workflow diagrams. No Fazah
production code is touched. The course slides are Arabic prose + English code; **this audit's prompts
and docs are in English** (the PL/SQL keywords/code are as they appear in the slides).

## Understand the workflow

See [Context Diagram and Audit Workflow](./misc/CONTEXT-DIAGRAM.md).

## Start auditing

**Use the Excel workbook — it's the one file you run the audit from:**
[`Fazah-Audit-Workbook.xlsx`](./Fazah-Audit-Workbook.xlsx). Three tabs: **How to use**, **Progress**
(one row per scenario), **Turn Results** (one row per turn, pre-filled with the exact prompt to
type). Every graded field is a **dropdown**; each scenario id links to its file.

1. Open the workbook and read the **How to use** tab.
2. On **Progress**, pick a scenario; note the lecture files to select (column F).
3. On **Turn Results**, work down that scenario's turns: type each `prompt_to_enter` into Fazah
   exactly as written, then fill `turn_result` (dropdown) + notes.
4. Save evidence (see [`EVIDENCE-NAMING.md`](./misc/EVIDENCE-NAMING.md)) and paste the link in the row.
5. When the scenario's turns are done, set its **Progress** row.

The scenario `.md` files ([`SCENARIO-INDEX.md`](./SCENARIO-INDEX.md)) hold the full **Expect** lines
for each turn — keep them open alongside the workbook.

## Before you run your first scenario

Read [`AUDITOR-INSTRUCTIONS.md`](./AUDITOR-INSTRUCTIONS.md) once — the nine rules, the four result
definitions, the Critical-fail triggers, and a short "what you'll see in Fazah" guide.

## The course under test

Eight lecture PDFs from an *Introduction to Database* course (Oracle PL/SQL):

| File | Topic |
|---|---|
| `Lec1.pdf` | Intro to PL/SQL: blocks, variables, data types, scope |
| `Lec2.pdf` | Conditional statements: IF / CASE |
| `Lec3.pdf` | Iterative statements: loops (simple / while / for / nested) |
| `Lec4.pdf` | `SELECT ... INTO`, `%TYPE`, `%ROWTYPE`, aggregates |
| `Lec5.pdf` | Explicit cursors |
| `Lec5_1.pdf` | Implicit cursors & SQL cursor attributes (⚠ `Lec5_11.pdf` is an identical duplicate) |
| `Lec6.pdf` | Procedures & Functions |
| `Lec7.pdf` | Exceptions (⚠ mostly image slides — thin extractable text) |

Two real quirks are used **only** in the ambiguity scenarios: `Lec5_1.pdf` ≡ `Lec5_11.pdf` are
byte-identical duplicates, and "the cursor lecture" is ambiguous between `Lec5` (explicit) and
`Lec5_1` (implicit). Every expected course fact is grounded in
[`COURSE-CONTENT-MAP.md`](./COURSE-CONTENT-MAP.md) — do not grade Fazah against PL/SQL knowledge that
isn't in these eight lectures.

## What's in this folder

| File | Purpose |
|---|---|
| [`Fazah-Audit-Workbook.xlsx`](./Fazah-Audit-Workbook.xlsx) | **Primary tool** — run the whole audit here; dropdowns + all 40 scenarios and every turn pre-filled |
| [`README.md`](./README.md) | This overview |
| [`AUDITOR-INSTRUCTIONS.md`](./AUDITOR-INSTRUCTIONS.md) | Rules, result definitions, Critical-fail triggers, UI guide |
| [`SCENARIO-INDEX.md`](./SCENARIO-INDEX.md) | All 40 scenarios grouped by category |
| [`COURSE-CONTENT-MAP.md`](./COURSE-CONTENT-MAP.md) | Ground-truth content per lecture |
| [`misc/CONTEXT-DIAGRAM.md`](./misc/CONTEXT-DIAGRAM.md) | Workflow diagrams |
| [`misc/DIVERSITY-COVERAGE-MATRIX.md`](./misc/DIVERSITY-COVERAGE-MATRIX.md) | Per-scenario dimensions + coverage proof |
| [`misc/AUDIT-PROGRESS-TEMPLATE.csv`](./misc/AUDIT-PROGRESS-TEMPLATE.csv) | One row per scenario |
| [`misc/TURN-RESULTS-TEMPLATE.csv`](./misc/TURN-RESULTS-TEMPLATE.csv) | One row per turn |
| [`misc/RESULTS-TEMPLATE.md`](./misc/RESULTS-TEMPLATE.md) | Human-readable results tables |
| [`misc/EVIDENCE-NAMING.md`](./misc/EVIDENCE-NAMING.md) | Screenshot / file naming convention |
| [`misc/FINAL-REPORT-TEMPLATE.md`](./misc/FINAL-REPORT-TEMPLATE.md) | End-of-audit report |
| [`misc/scenarios-embedded.csv`](./misc/scenarios-embedded.csv) | All 40 scenarios embedded in a CSV |
| [`misc/all-docs-embedded.csv`](./misc/all-docs-embedded.csv) | Every `.md` doc embedded in a CSV |
| [`scenarios/`](./scenarios/) | The 40 scenario files (`S001`–`S040`) |
| [`course-files/`](./course-files/) | The original course slides (source material) |

## Scenario groups

- **A — Source selection and grounding** (S001–S008)
- **B — Natural teacher input and instruction styles** (S009–S016)
- **C — Ambiguity, clarification, contradiction, and recovery** (S017–S022)
- **D — Course knowledge, explanation, and synthesis** (S023–S028)
- **E — Distinct artifact-generation workflows** (S029–S034)
- **F — Long multi-turn conversations** (S035–S040)
