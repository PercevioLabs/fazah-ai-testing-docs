# Fazah — Software Engineering Manual Human-Audit Suite

**Prepared by: Muhammad**

A realistic, diverse suite of **40 multi-turn conversations** (6–16 turns each) that a human auditor
runs inside Fazah, using a real "Introduction to Software Engineering" course (five theory decks).
Every scenario is a sustained conversation on one continuous teacher goal — no single-turn tests,
because a real teacher rarely stops after one message. The suite tests one question:

> **Can a real teacher complete a task in Fazah without repeatedly supervising or correcting it?**

Everything here is documentation, scenario design, audit templates, and workflow diagrams. No
Fazah production code is touched.

## Understand the workflow

See [Context Diagram and Audit Workflow](./misc/CONTEXT-DIAGRAM.md).

## Start auditing

**Use the Excel workbook — it's the one file you run the audit from:**
[`Fazah-Audit-Workbook.xlsx`](./Fazah-Audit-Workbook.xlsx). It has three tabs: **How to use**,
**Progress** (one row per scenario), and **Turn Results** (one row per turn, pre-filled with the
exact prompt to type). Every graded field is a **dropdown** — click the cell and pick a value.

1. Open the workbook and read the **How to use** tab.
2. On **Progress**, pick a scenario; note the course files to select (column F).
3. On **Turn Results**, work down that scenario's turns: type each `prompt_to_enter` into Fazah
   exactly as written, then fill `turn_result` (dropdown) + notes.
4. Save evidence (see [`EVIDENCE-NAMING.md`](./misc/EVIDENCE-NAMING.md)) and paste the link in the row.
5. When the scenario's turns are done, set its **Progress** row (status + overall_result + the
   four quality dropdowns).

The scenario `.md` files ([`SCENARIO-INDEX.md`](./SCENARIO-INDEX.md)) hold the full **Expect** lines
for each turn — keep them open alongside the workbook. The `*.csv` templates are the same data in
plain CSV (dropdowns are an Excel feature, so the workbook is what you fill in).

## Before you run your first scenario

Read [`AUDITOR-INSTRUCTIONS.md`](./AUDITOR-INSTRUCTIONS.md) once. It holds the nine rules, the four
result definitions, the Critical-fail triggers, and a short "what you'll see in Fazah" guide. The
scenarios deliberately **do not** repeat these.

## The course under test

Five theory decks from *Introduction to Software Engineering* (Sommerville-style):

| File | Displayed chapter | Topic |
|---|---|---|
| `Ch1 Introduction.pptx` | Chapter 1 | Introduction: SE, attributes of good software, ethics |
| `Ch2 SW Processes.pptx` | Chapter 2 | Software processes: waterfall, incremental, reuse, change, CMM |
| `Ch3 Req Eng.pptx` | **Chapter 4** | Requirements engineering (⚠ filename≠internal number) |
| `Ch4 Testing.pptx` | **Chapter 8** | Software testing (⚠ filename≠internal number) |
| `Ch5 Agile SW Dev.pptx` | **Chapter 3** | Agile software development (⚠ filename≠internal number) |

The filename-vs-internal-chapter mismatch (Ch3/Ch4/Ch5) is real and is used **only** in the
chapter-ambiguity scenario (S017) and where a scenario explicitly names a chapter number. Every
expected course fact is grounded in [`COURSE-CONTENT-MAP.md`](./COURSE-CONTENT-MAP.md) — do not
grade Fazah against Software Engineering knowledge that isn't in these five decks.

## What's in this folder

| File | Purpose |
|---|---|
| [`Fazah-Audit-Workbook.xlsx`](./Fazah-Audit-Workbook.xlsx) | **Primary tool** — run the whole audit here; dropdowns + all 40 scenarios and 338 turns pre-filled |
| [`README.md`](./README.md) | This overview |
| [`AUDITOR-INSTRUCTIONS.md`](./AUDITOR-INSTRUCTIONS.md) | Rules, result definitions, Critical-fail triggers, UI guide |
| [`SCENARIO-INDEX.md`](./SCENARIO-INDEX.md) | All 40 scenarios grouped by category |
| [`COURSE-CONTENT-MAP.md`](./COURSE-CONTENT-MAP.md) | Ground-truth content per deck |
| [`CONTEXT-DIAGRAM.md`](./misc/CONTEXT-DIAGRAM.md) | Workflow diagrams |
| [`DIVERSITY-COVERAGE-MATRIX.md`](./misc/DIVERSITY-COVERAGE-MATRIX.md) | Per-scenario dimensions + coverage proof |
| [`AUDIT-PROGRESS-TEMPLATE.csv`](./misc/AUDIT-PROGRESS-TEMPLATE.csv) | One row per scenario |
| [`TURN-RESULTS-TEMPLATE.csv`](./misc/TURN-RESULTS-TEMPLATE.csv) | One row per turn |
| [`RESULTS-TEMPLATE.md`](./misc/RESULTS-TEMPLATE.md) | Human-readable results tables |
| [`EVIDENCE-NAMING.md`](./misc/EVIDENCE-NAMING.md) | Screenshot / file naming convention |
| [`FINAL-REPORT-TEMPLATE.md`](./misc/FINAL-REPORT-TEMPLATE.md) | End-of-audit report |
| [`scenarios-embedded.csv`](./misc/scenarios-embedded.csv) | All 40 scenarios embedded in a CSV (full markdown per row) |
| [`all-docs-embedded.csv`](./misc/all-docs-embedded.csv) | Every `.md` doc (top-level + scenarios) embedded in a CSV |
| [`scenarios/`](./scenarios/) | The 40 scenario files (`S001`–`S040`) |
| [`course-files/`](./course-files/) | The original course slides (source material) |

## How results roll up

Six dashboard metrics (defined fully in [`FINAL-REPORT-TEMPLATE.md`](./misc/FINAL-REPORT-TEMPLATE.md)):
scenario pass rate, critical-failure count, correct source-use rate, teacher-ready output rate,
conversation success rate, clarification success rate. **Pass** and **Pass with small issue** are
always reported separately.

## Scenario groups

- **A — Source selection and grounding** (S001–S008)
- **B — Natural teacher input and instruction styles** (S009–S016)
- **C — Ambiguity, clarification, contradiction, and recovery** (S017–S022)
- **D — Course knowledge, explanation, and synthesis** (S023–S028)
- **E — Distinct artifact-generation workflows** (S029–S034)
- **F — Long multi-turn conversations** (S035–S040)
