# Fazah — Web Application Development (PHP) Manual Human-Audit Suite

**Prepared by: Muhammad**

A realistic, diverse suite of **40 long multi-turn conversations** (**10–30 turns each, average ~17**)
that a human auditor runs inside Fazah, using a real **Web Application Development** course taught
through **PHP** (plus concept modules on computer networks and web architecture). These conversations
are deliberately **big and challenging** — a hard stress test of accumulated context, sustained
selective editing, and long-range consistency. Every scenario is one continuous teacher goal. The
suite tests one question:

> **Can a real teacher complete a task in Fazah without repeatedly supervising or correcting it —
> even across a long, winding conversation?**

Everything here is documentation, scenario design, audit templates, and workflow diagrams. No Fazah
production code is touched. Prompts are English, written the way a real teacher types (messy/human).

## Understand the workflow

See [Context Diagram and Audit Workflow](./misc/CONTEXT-DIAGRAM.md).

## Start auditing

**Use the Excel workbook — it's the one file you run the audit from:**
[`Fazah-Audit-Workbook.xlsx`](./Fazah-Audit-Workbook.xlsx). Three tabs: **How to use**, **Progress**
(one row per scenario), **Turn Results** (one row per turn — ~676 rows, each pre-filled with the exact
prompt to type). Every graded field is a **dropdown**; each scenario id links to its file.

1. Open the workbook and read the **How to use** tab.
2. On **Progress**, pick a scenario; note the slide files to select (column F).
3. On **Turn Results**, work down that scenario's turns: type each `prompt_to_enter` into Fazah
   exactly as written, then fill `turn_result` (dropdown) + notes.
4. Save evidence (see [`EVIDENCE-NAMING.md`](./misc/EVIDENCE-NAMING.md)) and paste the link.
5. When the scenario's turns are done, set its **Progress** row.

The scenario `.md` files ([`SCENARIO-INDEX.md`](./SCENARIO-INDEX.md)) hold the full **Expect** lines
for each turn — keep them open alongside the workbook.

## Before you run your first scenario

Read [`AUDITOR-INSTRUCTIONS.md`](./AUDITOR-INSTRUCTIONS.md) once — the nine rules, the four result
definitions, the Critical-fail triggers, and a short "what you'll see in Fazah" guide.

## The course under test

15 PowerPoint decks (Web Application Development via PHP):

| File | Topic |
|---|---|
| `Module 1 - Computer Network for Web Developer.pptx` | Networks, OSI/TCP-IP, IP, DNS, HTTP verbs & status codes, ping/traceroute |
| `Module 3- Understanding Web Application Architecture.pptx` | Client-server, static vs dynamic, MVC |
| `php_syntax` · `php_comments` · `php_variables` · `php_datatypes` · `php_casting` · `php_numbers` | PHP fundamentals |
| `php_strings` · `php_operators (2)` · `php_if_else` · `php_switch` · `php_loops` · `php_arrays` · `php_forms` | PHP language + forms |

Two real quirks are used **only** in the ambiguity scenarios: **Module 2 does not exist** (only
Module 1 and Module 3), and `php_operators_presentation (2).pptx` carries a "(2)" version tag. Every
expected course fact is grounded in [`COURSE-CONTENT-MAP.md`](./COURSE-CONTENT-MAP.md) — do not grade
Fazah against PHP/web knowledge that isn't in these decks.

## What's in this folder

| File | Purpose |
|---|---|
| [`Fazah-Audit-Workbook.xlsx`](./Fazah-Audit-Workbook.xlsx) | **Primary tool** — run the whole audit here; dropdowns + all 40 scenarios and ~676 turns pre-filled |
| [`README.md`](./README.md) | This overview |
| [`AUDITOR-INSTRUCTIONS.md`](./AUDITOR-INSTRUCTIONS.md) | Rules, result definitions, Critical-fail triggers, UI guide |
| [`SCENARIO-INDEX.md`](./SCENARIO-INDEX.md) | All 40 scenarios grouped by category |
| [`COURSE-CONTENT-MAP.md`](./COURSE-CONTENT-MAP.md) | Ground-truth content per deck |
| [`misc/`](./misc/) | Context diagram, diversity matrix, evidence naming, results/final-report templates, CSV templates, embedded CSVs |
| [`scenarios/`](./scenarios/) | The 40 scenario files (`S001`–`S040`) |
| [`course-files/`](./course-files/) | The original course slides (source material) |

## Scenario groups

- **A — Source selection and grounding** (S001–S008)
- **B — Natural teacher input and instruction styles** (S009–S016)
- **C — Ambiguity, clarification, contradiction, and recovery** (S017–S022)
- **D — Course knowledge, explanation, and synthesis** (S023–S028)
- **E — Distinct artifact-generation workflows** (S029–S034)
- **F — Long multi-turn conversations** (S035–S040)
