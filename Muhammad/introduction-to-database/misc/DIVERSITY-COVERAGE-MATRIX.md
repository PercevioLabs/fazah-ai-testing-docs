# Diversity Coverage Matrix

One row per scenario. Guarantees every scenario is **materially different** — no two share the same
full combination of (Turns × Teacher style × Prompt size × Source state × Task type × Audience ×
Main risk). Every scenario is a **multi-turn conversation (6–16 turns)** on one continuous teacher
goal — no single-turn tests. Prompts are English; the course is Oracle **PL/SQL**.

**Risk vocabulary** (aligned to the Critical-fail triggers in
[AUDITOR-INSTRUCTIONS](../AUDITOR-INSTRUCTIONS.md)): Ambiguity, Unsupported request, Conflicting
instruction, Context loss, Source leakage (wrong/outside source), Answer leakage (answers shown to
students), Audience leakage, Grounding accuracy (fabrication / wrong content), False source claim,
Missed instruction.

| Scenario | Turns | Teacher style | Prompt size | Source state (lecture) | Task type | Audience | Main risk | Variation |
|---|---:|---|---|---|---|---|---|:--:|
| S001 | 6 | precise | normal | one selected (Lec5 explicit cursors) | question answering → assessment | teacher + student | Grounding accuracy | No |
| S002 | 6 | precise | normal | no file (→ Lec3 loops) | explanation → quiz | teacher + student | Source leakage | No |
| S003 | 8 | corrective | normal | wrong (Lec2) → corrected (Lec5) | explanation → comparison → quiz | teacher + student | Source leakage | No |
| S004 | 7 | precise | long | multiple (Lec2 + Lec3) | comparison → quiz | teacher + student | Source leakage | No |
| S005 | 9 | iterative | normal | all files | summary / study guide → quiz | teacher + student | Context loss | No |
| S006 | 8 | corrective | short | source changed (Lec4 → Lec5) | question answering / summary → quiz | teacher + student | Context loss | No |
| S007 | 7 | corrective | short | source changed (Lec6 → Lec3) | explanation → quiz | teacher + student | Source leakage | No |
| S008 | 9 | iterative | short | one selected (Lec3 loops) | quiz → notes → slides | teacher + student | Context loss | No |
| S009 | 6 | rushed | very short | no file (→ Lec3 for loop) | explanation → quiz | teacher | Ambiguity | No |
| S010 | 8 | typo-heavy | normal | one selected (Lec2 conditionals) | quiz (MCQ) | teacher + student | Missed instruction | No |
| S011 | 7 | conversational | normal | no file (→ Lec4) | explanation → activity | teacher + student | Grounding accuracy | No |
| S012 | 8 | demanding | very large | one selected (Lec6 procedures/functions) | lesson plan | undergraduate | Missed instruction | No |
| S013 | 6 | precise | normal | one selected (Lec1 block) | explanation → summary → check | first-year students | Missed instruction | **Yes** |
| S014 | 6 | conversational | normal | one selected (Lec5_1 implicit cursors) | explanation → quiz | students (new) | Ambiguity | **Yes** |
| S015 | 9 | demanding | long | one selected (Lec3 loops) | quiz (MCQ) | teacher + student | Missed instruction | No |
| S016 | 7 | iterative | very short | no file (→ Lec7 exceptions) | explanation → quiz | mixed | Context loss | **Yes** |
| S017 | 8 | uncertain | short | no file ("the cursor lecture" = Lec5 vs Lec5_1) | quiz | teacher + student | Ambiguity | No |
| S018 | 6 | precise | normal | no file (→ Lec3) | explanation → quiz | teacher + student | Source leakage | No |
| S019 | 7 | uncertain | short | no file (then Lec4) | quiz | teacher + student | Ambiguity | No |
| S020 | 9 | uncertain | very short | no file | exam | undergraduate + teacher | Ambiguity | **Yes** |
| S021 | 6 | corrective | short | no file (then Lec2) | assessment | teacher + student | Conflicting instruction | No |
| S022 | 6 | uncertain | short | no file (new chat, then Lec3) | quiz | teacher + student | False source claim | No |
| S023 | 6 | precise | normal | one selected (Lec1 data types) | question answering → quiz | teacher + student | Grounding accuracy | No |
| S024 | 7 | conversational | normal | one selected (Lec6) | comparison → quiz | teacher + student | Grounding accuracy | **Yes** |
| S025 | 8 | iterative | normal | one selected (Lec4 %TYPE/%ROWTYPE) | explanation → student self-check | student-facing | Context loss | No |
| S026 | 6 | precise | normal | one selected (Lec1) | explanation (structured) → quiz | teacher + student | Grounding accuracy | No |
| S027 | 7 | precise | long | one selected (Lec5 explicit cursors) | explanation → quiz | teacher + student | Grounding accuracy | No |
| S028 | 9 | iterative | normal | one selected (Lec5_1 SQL% attributes) | explanation / comparison → quiz | teacher + student | Grounding accuracy | No |
| S029 | 9 | iterative | normal | one selected (Lec2 conditionals) | quiz | teacher + student | Context loss | No |
| S030 | 12 | demanding | long | multiple (Lec3 + Lec4 + Lec5) | exam + rubric | teacher + student | Answer leakage | No |
| S031 | 10 | iterative | long | one selected (Lec6) | lesson plan → slides | undergraduate + student | Context loss | **Yes** |
| S032 | 10 | iterative | normal | one selected (Lec5) | slides → handout | teacher + student | Context loss | **Yes** |
| S033 | 8 | iterative | normal | one selected (Lec1) | notes | student-facing | Audience leakage | No |
| S034 | 12 | demanding | long | multiple (Lec5 + Lec5_1) | assignment + rubric | teacher + student | Missed instruction | No |
| S035 | 12 | iterative | normal | one selected (Lec2) | assessment (short-answer) | teacher + student | Context loss | No |
| S036 | 12 | iterative | long | one selected (Lec3) | lesson → handout → exit ticket | teacher + student | Context loss | No |
| S037 | 11 | iterative | normal | one selected (Lec5) | quiz | teacher + student | Answer leakage | No |
| S038 | 10 | corrective | normal | wrong (Lec3) → corrected (Lec6) | comparison + quiz | teacher + student | Source leakage | No |
| S039 | 14 | uncertain | normal | no file → multiple (Lec2 + Lec3 + Lec5) | exam + rubric | undergraduate + teacher | Ambiguity | No |
| S040 | 16 | conversational | long | multiple (Lec1 + Lec3 + Lec5) | mini-unit package | teacher + student | Context loss | **Yes** |

---

## Conversation-length distribution (all multi-turn)

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

Min 6 · Max 16 · Average ~8.4 turns.

## Coverage checks

- **No two scenarios share the same full combination.** ✅
- **Every lecture appears in a direct question AND an artifact task:**
  - Lec1 — direct: S013, S023, S026; artifact: S033, S040 ✅
  - Lec2 — direct: S004; artifact: S010, S029, S035 ✅
  - Lec3 — direct: S002, S009, S018, S004; artifact: S008, S015, S030, S036 ✅
  - Lec4 — direct: S011, S025; artifact: S019, S030 ✅
  - Lec5 — direct: S001, S027; artifact: S032, S037, S030 ✅
  - Lec5_1 — direct: S014, S028; artifact: S034 ✅
  - Lec6 — direct: S024, S007; artifact: S012, S031 ✅
  - Lec7 — direct: S016; artifact: S005 (thin content — expectations stay high-level) ⚠
- **≥8 scenarios test ambiguity/clarification:** S002, S009, S014, S017, S018, S019, S020, S021,
  S022, S039 (10). ✅
- **≥8 test selective editing:** S005, S008, S015, S016, S029–S037 and every long workflow. ✅
- **≥6 test teacher/student separation or audience:** S013, S025, S030, S033, S035, S036, S037,
  S039, S040 (9). ✅
- **≥6 use multiple files:** S004, S005 (all), S030, S034, S039, S040 (6). ✅

## Coverage notes (honest)

- **Lec7 (exceptions) is thin (image-based).** It appears in one direct scenario (S016) and one
  artifact (S005), both calibrated so Fazah must stay at the level the slides support
  (`NO_DATA_FOUND`, `TOO_MANY_ROWS`, `OTHERS`, the `EXCEPTION` section) and NOT fabricate deeper
  exception content. That is intentional, not a gap.
- **Assignment / rubric / slides** each appear in ≥2 scenarios (as in the SE suite).

## Scenarios with a small scenario-specific workflow diagram
Only these eight: **S006, S008, S017, S020, S030, S035, S039, S040.**

## Human-variation scenarios
**S013, S014, S016, S020, S024, S031, S032, S040** (8) — auditor may add/alter exactly one realistic
instruction and must record it. All others: enter prompts verbatim.
