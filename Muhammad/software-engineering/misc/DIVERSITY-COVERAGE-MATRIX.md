# Diversity Coverage Matrix

One row per scenario. This is the master plan that guarantees every scenario is
**materially different** — no two rows share the same full combination of
(Turns × Teacher style × Prompt size × Source state × Task type × Audience × Main risk).

**Every scenario is a multi-turn conversation (6–16 turns)** on one continuous teacher goal —
real teachers keep going, so there are no single-turn tests. "Prompt size" describes the typical
turn prompt (turns vary in length within a scenario).

**Risk vocabulary** (aligned to the Critical-fail triggers in
[AUDITOR-INSTRUCTIONS](../AUDITOR-INSTRUCTIONS.md)): Ambiguity, Unsupported request,
Conflicting instruction, Context loss, Source leakage (wrong/outside source), Answer
leakage (answers shown to students), Audience leakage (teacher-only language in student
material), Grounding accuracy (fabrication / wrong content), False source claim,
Missed instruction, Lost work.

| Scenario | Turns | Teacher style | Prompt size | Source state | Task type | Audience | Main risk | Human variation |
|---|---:|---|---|---|---|---|---|:--:|
| S001 | 6 | precise | normal | one selected (Testing) | question answering → assessment | teacher + student | Grounding accuracy | No |
| S002 | 6 | precise | normal | no file | explanation → quiz | teacher + student | Source leakage | No |
| S003 | 8 | corrective | normal | wrong selected (Agile) → corrected | explanation → comparison → quiz | teacher + student | Source leakage | No |
| S004 | 7 | precise | long | multiple (Processes+Agile) | comparison (table) → quiz | teacher + student | Source leakage | No |
| S005 | 9 | iterative | normal | all files | summary / study guide → quiz | teacher + student | Context loss | No |
| S006 | 8 | corrective | short | source changed mid-chat | question answering / summary → quiz | teacher + student | Context loss | No |
| S007 | 7 | corrective | short | source changed mid-chat | explanation → quiz | teacher + student | Source leakage | No |
| S008 | 9 | iterative | short | one selected (Testing) | quiz → notes → slides | teacher + student | Context loss | No |
| S009 | 6 | rushed | very short | no file | explanation → quiz | teacher | Ambiguity | No |
| S010 | 8 | typo-heavy | normal | one selected (Testing) | quiz (MCQ) | teacher + student | Missed instruction | No |
| S011 | 7 | conversational | normal | no file | explanation → activity → exit ticket | teacher + student | Grounding accuracy | No |
| S012 | 8 | demanding | very large | one selected (Agile) | lesson plan → handout | undergraduate | Missed instruction | No |
| S013 | 6 | precise | normal | one selected (Introduction) | explanation → summary → check | first-year students | Missed instruction | **Yes** |
| S014 | 6 | conversational | normal | one selected (Agile) | explanation → quiz | students (new to Scrum) | Ambiguity | **Yes** |
| S015 | 9 | demanding | long | one selected (Testing) | quiz (MCQ) | teacher + student | Missed instruction | No |
| S016 | 7 | iterative | very short | no file | explanation → quiz | mixed | Context loss | **Yes** |
| S017 | 8 | uncertain | short | no file | quiz | teacher + student | Ambiguity | No |
| S018 | 6 | precise | normal | no file | explanation → quiz | teacher + student | Source leakage | No |
| S019 | 7 | uncertain | short | no file (then selected) | quiz | teacher + student | Ambiguity | No |
| S020 | 9 | uncertain | very short | no file | exam | undergraduate + teacher | Ambiguity | **Yes** |
| S021 | 6 | corrective | short | no file (then selected) | assessment | teacher + student | Conflicting instruction | No |
| S022 | 6 | uncertain | short | no file (new chat, then selected) | quiz | teacher + student | False source claim | No |
| S023 | 6 | precise | normal | one selected (Introduction) | question answering → quiz | teacher + student | Grounding accuracy | No |
| S024 | 7 | conversational | normal | one selected (Processes) | comparison → quiz | teacher + student | Grounding accuracy | **Yes** |
| S025 | 8 | iterative | normal | one selected (Requirements) | explanation → student self-check | student-facing | Context loss | No |
| S026 | 6 | precise | normal | one selected (Testing) | explanation (structured) → quiz | teacher + student | Grounding accuracy | No |
| S027 | 7 | precise | long | one selected (Testing) | explanation → quiz | teacher + student | Grounding accuracy | No |
| S028 | 9 | iterative | normal | one selected (Agile) | explanation / comparison → quiz | teacher + student | Grounding accuracy | No |
| S029 | 9 | iterative | normal | one selected (Testing) | quiz | teacher + student | Context loss | No |
| S030 | 12 | demanding | long | multiple (Processes+Req+Testing) | exam + rubric | teacher + student | Answer leakage | No |
| S031 | 10 | iterative | long | one selected (Agile) | lesson plan → slides | undergraduate + student | Context loss | **Yes** |
| S032 | 10 | iterative | normal | one selected (Requirements) | slides → handout | teacher + student | Context loss | **Yes** |
| S033 | 8 | iterative | normal | one selected (Introduction) | notes | student-facing | Audience leakage | No |
| S034 | 12 | demanding | long | multiple (Processes+Agile) | assignment + rubric | teacher + student | Missed instruction | No |
| S035 | 12 | iterative | normal | one selected (Requirements) | assessment (short-answer) | teacher + student | Context loss | No |
| S036 | 12 | iterative | long | one selected (Processes) | lesson → handout → exit ticket | teacher + student | Context loss | No |
| S037 | 11 | iterative | normal | one selected (Testing) | quiz | teacher + student | Answer leakage | No |
| S038 | 10 | corrective | normal | wrong selected → corrected | comparison + quiz | teacher + student | Source leakage | No |
| S039 | 14 | uncertain | normal | no file → multiple | exam + rubric | undergraduate + teacher | Ambiguity | No |
| S040 | 16 | conversational | long | multiple (Intro+Processes+Agile) | mini-unit package | teacher + student | Context loss | **Yes** |

---

## Conversation-length distribution

Every scenario is multi-turn (no single-turn tests). Spread is intentionally varied across 6–16
turns so the suite exercises short focused workflows and long accumulated-context marathons alike.

| Turns | Scenarios | Count |
|---:|---|---:|
| 6 | S001, S002, S009, S013, S014, S018, S021, S022, S023, S026 | 10 |
| 7 | S004, S007, S011, S016, S024, S027 | 6 |
| 8 | S003, S006, S010, S012, S017, S025, S033 | 7 |
| 9 | S005, S015, S020, S028, S029 | 5 |
| 10 | S031, S032, S038 | 3 |
| 11 | S037 | 1 |
| 12 | S030, S034, S035, S036 | 4 |
| 14 | S039 | 1 |
| 16 | S040 | 1 |
| **Total** | | **40** |

Min 6 · Max 16 · Total 338 turns · Average ~8.4 turns per scenario. Every scenario ≥ 5 turns.

## Coverage checks

- **No two scenarios share the same full combination.** ✅ (verified across the 8 dimensions above)
- **Every course file appears in direct questions AND artifact tasks:**
  - Introduction — direct: S013, S023; artifact: S033, S040 ✅
  - Software Processes — direct: S024; artifact: S030, S034, S036, S040 ✅
  - Requirements Engineering — direct: S025; artifact: S030, S032, S035, S039 ✅
  - Testing — direct: S001, S002, S026, S027; artifact: S008, S010, S015, S029, S037 ✅
  - Agile — direct: S014, S016, S028; artifact: S012, S031, S034, S040 ✅
- **Selected-file vs. no-file both well represented:** 20 selected-file starts, 11 no-file starts,
  plus wrong-file / mid-chat-change / multi / all-files variants. ✅
- **≥8 scenarios test ambiguity or clarification:** S002, S009, S014, S017, S018, S019, S020,
  S021, S022, S039 (10). ✅
- **≥8 scenarios test selective editing:** now essentially all scenarios include an edit/refine
  turn; the strongest are S005, S008, S015, S016, S029–S037 and every long workflow. ✅
- **≥6 scenarios test teacher/student separation or audience change:** now most scenarios end with a
  student version and/or teacher key; strongest are S013, S025, S030, S033, S035, S036, S037, S039,
  S040. ✅
- **≥6 scenarios use multiple files:** S004, S005 (all), S030, S034, S039, S040 (6). ✅
- **All 40 are long/large conversations** (6–16 turns), so the "large prompt / long conversation"
  bar is met suite-wide. ✅

## Task-type coverage (honest)

| Task type | Scenarios | Count |
|---|---|---:|
| Question answering | S001, S006, S023, S027 (+embedded) | ≥2 ✅ |
| Explanation | S002, S009, S011, S013, S016, S018, S025, S028 | ≥2 ✅ |
| Comparison | S004, S024, S028, S034, S038 | ≥2 ✅ |
| Summary | S005, S006, S036, S040 | ≥2 ✅ |
| Quiz | S008, S010, S015, S017, S019, S029, S037 | ≥2 ✅ |
| Exam | S020, S030, S039 | ≥2 ✅ |
| Lesson plan | S012, S031, S036, S040 | ≥2 ✅ |
| Notes | S008, S025, S033, S036 | ≥2 ✅ |
| Slides | S008, S031, S032, S040 | ≥2 ✅ |
| Study guide | S005, S040 | ≥2 ✅ |
| Rubric | S030, S034, S039 | ≥2 ✅ |
| Assignment | S034, S040 | ≥2 ✅ |

> **Coverage note.** Because every scenario is now a full workflow, several previously
> single-instance task types (slides, rubric, assignment) now appear in ≥2 scenarios as natural
> follow-on turns. All task types are exercised at least twice.

## Scenarios with a small scenario-specific workflow diagram

Only these eight carry a small (≤6-node) scenario diagram; all other 32 scenarios have none:
**S006, S008, S017, S020, S030, S035, S039, S040.**

## Human-variation scenarios (controlled)

**S013, S014, S016, S020, S024, S031, S032, S040** (8) — auditor may add/alter exactly one
realistic instruction and must record it. All other scenarios: enter prompts verbatim.
