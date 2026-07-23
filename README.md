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

See [Context Diagram and Audit Workflow](./CONTEXT-DIAGRAM.md).

## Start auditing

1. Open [`SCENARIO-INDEX.md`](./SCENARIO-INDEX.md).
2. Choose an assigned scenario.
3. Follow the scenario setup and prompts.
4. Save evidence (see [`EVIDENCE-NAMING.md`](./EVIDENCE-NAMING.md)).
5. Record the result in the progress and turn-results templates
   ([`AUDIT-PROGRESS-TEMPLATE.csv`](./AUDIT-PROGRESS-TEMPLATE.csv),
   [`TURN-RESULTS-TEMPLATE.csv`](./TURN-RESULTS-TEMPLATE.csv)).

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
| [`README.md`](./README.md) | This overview |
| [`AUDITOR-INSTRUCTIONS.md`](./AUDITOR-INSTRUCTIONS.md) | Rules, result definitions, Critical-fail triggers, UI guide |
| [`SCENARIO-INDEX.md`](./SCENARIO-INDEX.md) | All 40 scenarios grouped by category |
| [`COURSE-CONTENT-MAP.md`](./COURSE-CONTENT-MAP.md) | Ground-truth content per deck |
| [`CONTEXT-DIAGRAM.md`](./CONTEXT-DIAGRAM.md) | Workflow diagrams |
| [`DIVERSITY-COVERAGE-MATRIX.md`](./DIVERSITY-COVERAGE-MATRIX.md) | Per-scenario dimensions + coverage proof |
| [`AUDIT-PROGRESS-TEMPLATE.csv`](./AUDIT-PROGRESS-TEMPLATE.csv) | One row per scenario |
| [`TURN-RESULTS-TEMPLATE.csv`](./TURN-RESULTS-TEMPLATE.csv) | One row per turn |
| [`RESULTS-TEMPLATE.md`](./RESULTS-TEMPLATE.md) | Human-readable results tables |
| [`EVIDENCE-NAMING.md`](./EVIDENCE-NAMING.md) | Screenshot / file naming convention |
| [`FINAL-REPORT-TEMPLATE.md`](./FINAL-REPORT-TEMPLATE.md) | End-of-audit report |
| [`scenarios-embedded.csv`](./scenarios-embedded.csv) | All 40 scenarios embedded in a CSV (full markdown per row) |
| [`all-docs-embedded.csv`](./all-docs-embedded.csv) | Every `.md` doc (top-level + scenarios) embedded in a CSV |
| [`scenarios/`](./scenarios/) | The 40 scenario files (`S001`–`S040`) |

## How results roll up

Six dashboard metrics (defined fully in [`FINAL-REPORT-TEMPLATE.md`](./FINAL-REPORT-TEMPLATE.md)):
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
