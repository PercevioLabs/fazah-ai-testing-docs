# Diversity Coverage Matrix

One row per scenario. Guarantees every scenario is **materially different** — no two share the same
full combination of (Turns × Teacher style × Prompt size × Source state × Task type × Audience ×
Main risk). Prompts are English; course = **Web Application Development (PHP)**.

**These conversations are deliberately LONG (10–30 turns, average ~17)** — a harder stress test of
accumulated context, sustained selective editing, and long-range consistency than the earlier
suites. Every turn is still a real refinement of the same teacher goal (no padding).

**Risk vocabulary:** Ambiguity, Unsupported request, Conflicting instruction, Context loss, Source
leakage, Answer leakage, Audience leakage, Grounding accuracy, False source claim, Missed instruction.

| Scenario | Turns | Teacher style | Prompt size | Source state (topic) | Task type | Audience | Main risk | Variation |
|---|---:|---|---|---|---|---|---|:--:|
| S001 | 12 | precise | normal | one selected (php_loops) | question answering → assessment | teacher + student | Grounding accuracy | No |
| S002 | 12 | precise | normal | no file (→ php_operators) | explanation → quiz | teacher + student | Source leakage | No |
| S003 | 16 | corrective | normal | wrong (php_loops) → corrected (php_forms) | explanation → comparison → quiz | teacher + student | Source leakage | No |
| S004 | 14 | precise | long | multiple (php_if_else + php_switch) | comparison → quiz | teacher + student | Source leakage | No |
| S005 | 20 | iterative | normal | all files | summary / study guide → quiz | teacher + student | Context loss | No |
| S006 | 16 | corrective | short | source changed (Module 1 → php_forms) | question answering / summary → quiz | teacher + student | Context loss | No |
| S007 | 14 | corrective | short | source changed (php_arrays → php_strings) | explanation → quiz | teacher + student | Source leakage | No |
| S008 | 18 | iterative | short | one selected (php_variables) | quiz → notes → slides | teacher + student | Context loss | No |
| S009 | 10 | rushed | very short | no file (→ php_loops for loop) | explanation → quiz | teacher | Ambiguity | No |
| S010 | 16 | typo-heavy | normal | one selected (php_datatypes) | quiz (MCQ) | teacher + student | Missed instruction | No |
| S011 | 14 | conversational | normal | no file (→ php_strings) | explanation → activity | teacher + student | Grounding accuracy | No |
| S012 | 18 | demanding | very large | one selected (Module 3 architecture/MVC) | lesson plan | undergraduate | Missed instruction | No |
| S013 | 12 | precise | normal | one selected (php_syntax) | explanation → summary → check | first-year students | Missed instruction | **Yes** |
| S014 | 12 | conversational | normal | one selected (Module 1 HTTP) | explanation → quiz | students (new) | Ambiguity | **Yes** |
| S015 | 18 | demanding | long | one selected (php_operators) | quiz (MCQ) | teacher + student | Missed instruction | No |
| S016 | 14 | iterative | very short | no file (→ php_casting) | explanation → quiz | mixed | Context loss | **Yes** |
| S017 | 16 | uncertain | short | no file ("Module 2" — does not exist) | quiz | teacher + student | Unsupported request | No |
| S018 | 12 | precise | normal | no file (→ php_numbers) | explanation → quiz | teacher + student | Source leakage | No |
| S019 | 14 | uncertain | short | no file (then php_forms) | quiz | teacher + student | Ambiguity | No |
| S020 | 18 | uncertain | very short | no file | exam | undergraduate + teacher | Ambiguity | **Yes** |
| S021 | 12 | corrective | short | no file (then php_if_else) | assessment | teacher + student | Conflicting instruction | No |
| S022 | 12 | uncertain | short | no file (new chat, then php_loops) | quiz | teacher + student | False source claim | No |
| S023 | 12 | precise | normal | one selected (php_datatypes) | question answering → quiz | teacher + student | Grounding accuracy | No |
| S024 | 14 | conversational | normal | one selected (php_forms GET vs POST) | comparison → quiz | teacher + student | Grounding accuracy | **Yes** |
| S025 | 16 | iterative | normal | one selected (php_strings) | explanation → student self-check | student-facing | Context loss | No |
| S026 | 12 | precise | normal | one selected (php_comments) | explanation (structured) → quiz | teacher + student | Grounding accuracy | No |
| S027 | 14 | precise | long | one selected (php_forms) | explanation → quiz | teacher + student | Grounding accuracy | No |
| S028 | 18 | iterative | normal | one selected (Module 1 HTTP) | explanation / synthesis → quiz | teacher + student | Grounding accuracy | No |
| S029 | 18 | iterative | normal | one selected (php_if_else) | quiz | teacher + student | Context loss | No |
| S030 | 24 | demanding | long | multiple (php_loops + php_arrays + php_forms) | exam + rubric | teacher + student | Answer leakage | No |
| S031 | 20 | iterative | long | one selected (php_arrays) | lesson plan → slides | undergraduate + student | Context loss | **Yes** |
| S032 | 20 | iterative | normal | one selected (php_operators) | slides → handout | teacher + student | Context loss | **Yes** |
| S033 | 16 | iterative | normal | one selected (php_syntax) | notes | student-facing | Audience leakage | No |
| S034 | 24 | demanding | long | multiple (php_forms + php_arrays) | assignment + rubric | teacher + student | Missed instruction | No |
| S035 | 24 | iterative | normal | one selected (php_loops) | assessment (short-answer) | teacher + student | Context loss | No |
| S036 | 24 | iterative | long | one selected (php_strings) | lesson → handout → exit ticket | teacher + student | Context loss | No |
| S037 | 22 | iterative | normal | one selected (php_arrays) | quiz | teacher + student | Answer leakage | No |
| S038 | 20 | corrective | normal | wrong (php_strings) → corrected (php_arrays) | comparison + quiz | teacher + student | Source leakage | No |
| S039 | 28 | uncertain | normal | no file → multiple (php_if_else + php_switch + php_loops) | exam + rubric | undergraduate + teacher | Ambiguity | No |
| S040 | 30 | conversational | long | multiple (Module 3 + php_forms + php_arrays) | mini-unit package | teacher + student | Context loss | **Yes** |

---

## Conversation-length distribution (all deliberately long)

| Turns | Scenarios | Count |
|---:|---|---:|
| 10 | S009 | 1 |
| 12 | S001, S002, S013, S014, S018, S021, S022, S023, S026 | 9 |
| 14 | S004, S007, S011, S016, S019, S024, S027 | 7 |
| 16 | S003, S006, S010, S017, S025, S033 | 6 |
| 18 | S008, S012, S015, S020, S028, S029 | 6 |
| 20 | S005, S031, S032, S038 | 4 |
| 22 | S037 | 1 |
| 24 | S030, S034, S035, S036 | 4 |
| 28 | S039 | 1 |
| 30 | S040 | 1 |
| **Total** | | **40** |

**Min 10 · Max 30 · Total ~676 turns · Average ~16.9 turns per scenario** — roughly double the
earlier suites, per the "even more challenging, big chats" brief.

## Coverage checks

- **No two scenarios share the same full combination.** ✅
- **All 15 files appear:** Module 1 (S006, S014, S028, S034-adjacent), Module 3 (S012, S040),
  php_syntax (S013, S033), php_comments (S026), php_variables (S008), php_datatypes (S010, S023),
  php_casting (S016), php_numbers (S018), php_strings (S007, S011, S025, S036, S038), php_operators
  (S002, S015, S032), php_if_else (S004, S021, S029, S039), php_switch (S004, S039), php_loops
  (S001, S003, S009, S022, S030, S035, S039), php_arrays (S030, S031, S034, S037, S038, S040),
  php_forms (S003, S006, S019, S024, S027, S030, S034, S040). ✅
- **≥8 ambiguity/clarification:** S002, S009, S014, S017, S018, S019, S020, S021, S022, S039 (10). ✅
- **≥8 selective editing:** all long workflows plus S005, S008, S015, S016, S029–S037. ✅
- **≥6 teacher/student separation:** S013, S025, S030, S033, S035, S036, S037, S039, S040 (9). ✅
- **≥6 multiple files:** S004, S005 (all), S030, S034, S039, S040 (6). ✅

## Coverage notes (honest)
- **Module 3** appears mainly in a lesson (S012) and the package (S040); the diagram-heavy modules
  are used at the concept level the slides support. **S017 tests a genuinely missing file (Module 2)**
  — Fazah must flag it, not fabricate.

## Scenarios with a small workflow diagram
Only: **S006, S008, S017, S020, S030, S035, S039, S040.**

## Human-variation scenarios
**S013, S014, S016, S020, S024, S031, S032, S040** (8).
