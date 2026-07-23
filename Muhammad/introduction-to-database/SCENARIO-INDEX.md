# Scenario Index

All 40 scenarios, grouped by category. Every scenario is a **multi-turn teacher conversation**
(6–16 turns) on one continuous goal. "Files selected" is the starting selection (some scenarios
change/add files mid-chat). "Diagram" marks the eight scenarios with a scenario-specific workflow
diagram. Course = Oracle **PL/SQL**.

> Per-scenario dimensions: [misc/DIVERSITY-COVERAGE-MATRIX.md](./misc/DIVERSITY-COVERAGE-MATRIX.md).

## Source selection and grounding

| ID | Scenario | Files selected | Turns | Main behavior | Diagram |
|---|---|---|---:|---|:--:|
| S001 | [Selected cursor lecture, direct concept question](./scenarios/S001-selected-cursor-file-direct-question.md) | Lec5 | 6 | Grounds an explicit-cursor answer and builds it into assessment | — |
| S002 | [No selected file, clear loops topic](./scenarios/S002-no-file-clear-loops-topic.md) | none | 6 | Auto-selects the loops lecture and stays on it | — |
| S003 | [Wrong selected file conflicts with topic](./scenarios/S003-wrong-file-topic-conflict.md) | Lec2 | 8 | Detects a mismatch, recovers, then builds correctly | — |
| S004 | [Two lectures for a structured comparison](./scenarios/S004-two-files-structured-comparison.md) | Lec2, Lec3 | 7 | Synthesizes conditionals vs loops, iterates on the table | — |
| S005 | [All lectures: course revision guide](./scenarios/S005-all-files-revision-guide.md) | all eight | 9 | Broad coverage + selective expansion + quiz | — |
| S006 | [Source changes during the conversation](./scenarios/S006-source-changes-midchat.md) | Lec4 → Lec5 | 8 | Resolves "the second file" after a source switch | ✅ |
| S007 | [Explicit selection overrides source history](./scenarios/S007-explicit-selection-overrides-history.md) | Lec6 → Lec3 | 7 | Current explicit source beats recent context | — |
| S008 | ["Use the same source" continuity](./scenarios/S008-use-same-source-continuity.md) | Lec3 | 9 | Retains one source across many artifact types | ✅ |

## Natural teacher input and instruction styles

| ID | Scenario | Files selected | Turns | Main behavior | Diagram |
|---|---|---|---:|---|:--:|
| S009 | [Extremely short prompts](./scenarios/S009-extremely-short-prompt.md) | none | 6 | Recovers intent from minimal language, repeatedly | — |
| S010 | [Typo-heavy assessment prompts](./scenarios/S010-typo-heavy-assessment.md) | Lec2 | 8 | Tolerates typos across a whole quiz workflow | — |
| S011 | [Conversational classroom problem](./scenarios/S011-conversational-classroom-problem.md) | none | 7 | Natural intent + pedagogical build-out | — |
| S012 | [Large instruction-heavy lesson request](./scenarios/S012-large-instruction-heavy-lesson.md) | Lec6 | 8 | Many constraints from one prompt, then refined | — |
| S013 | [Auditor adds one realistic instruction](./scenarios/S013-auditor-adds-one-instruction.md) | Lec1 | 6 | Honors an auditor-added constraint and continues | — |
| S014 | [Auditor writes the prompt](./scenarios/S014-auditor-writes-prompt.md) | Lec5_1 | 6 | Robust to realistic human wording | — |
| S015 | [Dense assessment constraints](./scenarios/S015-dense-assessment-constraints.md) | Lec3 | 9 | Constraint compliance + targeted improvement | — |
| S016 | [Informal refinement language](./scenarios/S016-informal-refinement-language.md) | none | 7 | Informal edits preserve the definition | — |

## Ambiguity, clarification, contradiction, and recovery

| ID | Scenario | Files selected | Turns | Main behavior | Diagram |
|---|---|---|---:|---|:--:|
| S017 | [Ambiguous "the cursor lecture"](./scenarios/S017-ambiguous-cursor-lecture.md) | none | 8 | Resolves explicit-vs-implicit cursor file ambiguity | ✅ |
| S018 | [Clear topic, indirect source name](./scenarios/S018-clear-topic-indirect-source.md) | none | 6 | Maps "the lecture about loops" to the right file | — |
| S019 | ["Use these slides" with no active source](./scenarios/S019-use-these-slides-no-source.md) | none | 7 | Asks which slides; resolves the deictic reference | — |
| S020 | [Underspecified exam request](./scenarios/S020-underspecified-exam.md) | none | 9 | Clarifies efficiently, then builds and verifies | ✅ |
| S021 | [Directly conflicting item counts](./scenarios/S021-conflicting-item-counts.md) | none | 6 | Detects a contradiction, then completes cleanly | — |
| S022 | ["Same sources as before" in a new chat](./scenarios/S022-same-sources-new-chat.md) | none (new chat) | 6 | Doesn't invent context; recovers on selection | — |

## Course knowledge, explanation, and synthesis

| ID | Scenario | Files selected | Turns | Main behavior | Diagram |
|---|---|---|---:|---|:--:|
| S023 | [PL/SQL data types](./scenarios/S023-plsql-data-types.md) | Lec1 | 6 | Correctly lists the data types, then builds | — |
| S024 | [Procedure vs function](./scenarios/S024-procedure-vs-function.md) | Lec6 | 7 | Comparison + in-framing application | — |
| S025 | [%TYPE vs %ROWTYPE](./scenarios/S025-type-vs-rowtype.md) | Lec4 | 8 | Definitions → HR example → student self-check | — |
| S026 | [Variable, constant, NOT NULL, DEFAULT](./scenarios/S026-variable-constant-notnull-default.md) | Lec1 | 6 | Distinguishes all four, then assesses | — |
| S027 | [Cursor lifecycle and attributes](./scenarios/S027-cursor-lifecycle-attributes.md) | Lec5 | 7 | Lifecycle + attribute examples, then questions | — |
| S028 | [SQL cursor attributes synthesis](./scenarios/S028-sql-cursor-attributes-synthesis.md) | Lec5_1 | 9 | Multi-step synthesis inside one source | — |

## Distinct artifact-generation workflows

| ID | Scenario | Files selected | Turns | Main behavior | Diagram |
|---|---|---|---:|---|:--:|
| S029 | [Ten-question conditionals quiz](./scenarios/S029-ten-question-conditionals-quiz.md) | Lec2 | 9 | Exactly ten Qs; reorder/refine without content loss | — |
| S030 | [Multi-file 20-point exam](./scenarios/S030-multi-file-20-point-exam.md) | Lec3, Lec4, Lec5 | 12 | Balanced multi-source exam; verify/replace/student | ✅ |
| S031 | [Procedures & functions lesson plan](./scenarios/S031-procedures-lesson-plan.md) | Lec6 | 10 | Iterative lesson design into teaching assets | — |
| S032 | [Cursor teaching slide deck](./scenarios/S032-cursor-slide-deck.md) | Lec5 | 10 | Slide-specific selective edits | — |
| S033 | [Student notes from the intro lecture](./scenarios/S033-student-notes-intro.md) | Lec1 | 8 | Audience + length constraints; answer separation | — |
| S034 | [Explicit vs implicit cursor assignment with rubric](./scenarios/S034-explicit-vs-implicit-assignment-rubric.md) | Lec5, Lec5_1 | 12 | Assignment + rubric continuity | — |

## Long multi-turn conversations

| ID | Scenario | Files selected | Turns | Main behavior | Diagram |
|---|---|---|---:|---|:--:|
| S035 | [Complete conditionals assessment lifecycle](./scenarios/S035-conditionals-assessment-lifecycle.md) | Lec2 | 12 | Selective edits, count preservation, audience split | ✅ |
| S036 | [Loops lesson transformed into teaching assets](./scenarios/S036-loops-lesson-into-teaching-assets.md) | Lec3 | 12 | One source → several connected artifacts | — |
| S037 | [Cursor quiz quality refinement](./scenarios/S037-cursor-quiz-quality-refinement.md) | Lec5 | 11 | Quality self-review + answer separation | — |
| S038 | [Source mismatch, correction, and recovery](./scenarios/S038-source-mismatch-correction-recovery.md) | Lec3 → Lec6 | 10 | Graceful recovery after a source conflict | — |
| S039 | [Ambiguous exam via clarification and revision](./scenarios/S039-ambiguous-exam-clarification-revision.md) | none → Lec2, Lec3, Lec5 | 14 | Clarify, select, revise, verify totals | ✅ |
| S040 | [Complete mini course package](./scenarios/S040-complete-course-package-long-conversation.md) | Lec1, Lec3, Lec5 | 16 | Long-range multi-source, multi-artifact inventory | ✅ |
