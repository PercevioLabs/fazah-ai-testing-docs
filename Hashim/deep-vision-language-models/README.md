# Fazah — Deep Vision Language Models (AI623) Audit Suite

**Prepared by: Hashim**

A realistic, diverse suite of **40 multi-turn conversations** (6–16 turns each) for auditing the
Fazah teacher chat, built on a real LUMS MS course — **AI623: Deep Vision Language Models**
(Spring 2026): transformers → VAEs → score-based models → diffusion (DDPM/DDIM) → flow matching →
autoregressive generation + alignment (RLHF/PPO/DPO/GRPO) → vision-language models (ViT/CLIP).
Every scenario is a sustained conversation on one continuous teacher goal. The suite tests one
question:

> **Can a real teacher complete a task in Fazah without repeatedly supervising or correcting it?**

This suite follows the same format as the Software Engineering / Database / Web-Dev suites, with
two additions:

1. **A math-heavy course.** Many scenarios check formulas and *numeric answers* (the course files
   include fully worked problems with boxed answers), so grounding failures are objectively
   checkable — Fazah's arithmetic can be marked right or wrong, not just "plausible".
2. **A deliberate unreadable-source edge case.** One uploaded file
   (`14_handwritten_class_notes_L2.pdf`) is scanned handwriting with **zero extractable text**.
   Scenario S017 tests whether Fazah is honest about a source it cannot read.

## Contents

| File | What it is |
|---|---|
| [`SCENARIO-INDEX.md`](./SCENARIO-INDEX.md) | All 40 scenarios by category, with files + turn counts |
| [`COURSE-CONTENT-MAP.md`](./COURSE-CONTENT-MAP.md) | What each course file contains — the grounding reference |
| [`AUDITOR-INSTRUCTIONS.md`](./AUDITOR-INSTRUCTIONS.md) | The nine rules, result definitions, critical-fail triggers |
| [`scenarios/`](./scenarios/) | The 40 scenario scripts (S001–S040) |
| [`Fazah-Audit-Workbook.xlsx`](./Fazah-Audit-Workbook.xlsx) | Run the audit from here — Progress + Turn Results tabs, dropdowns |
| [`course-files/`](./course-files/) | The original course files, named as uploaded to Fazah |
| [`results/`](./results/) | **Executed run** — full API-driven transcripts + per-turn grading + findings report |
| [`misc/`](./misc/) | Templates: results, evidence naming, progress CSVs |

## Start auditing

1. Open [`Fazah-Audit-Workbook.xlsx`](./Fazah-Audit-Workbook.xlsx) and read the **How to use** tab.
2. On **Progress**, pick a scenario; note the course files to select.
3. On **Turn Results**, work down that scenario's turns: type each `prompt_to_enter` into Fazah
   exactly as written, then fill `turn_result` (dropdown) + a short note.
4. Judge against [`AUDITOR-INSTRUCTIONS.md`](./AUDITOR-INSTRUCTIONS.md) and verify facts against
   [`COURSE-CONTENT-MAP.md`](./COURSE-CONTENT-MAP.md).

## The executed baseline run

This suite has already been executed once end-to-end against production
(course: *AI623 — Deep Vision Language Models*, teacher: demo account) by driving the Fazah API
directly — every scenario's turns sent in order, every response captured. See
[`results/`](./results/) for the transcripts, per-turn verdicts, and the findings report. A human
re-run through the UI is still valuable (the UI layer — cards, source pickers, artifact studio —
is not exercised by the API run).
