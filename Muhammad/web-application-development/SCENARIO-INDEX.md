# Scenario Index

All 40 scenarios, grouped by category. Every scenario is a **long multi-turn conversation
(10–30 turns)** on one continuous goal. "Files selected" is the starting selection (some change/add
files mid-chat). "Diagram" marks the eight scenarios with a workflow diagram. Course = **PHP / Web App Dev**.

> Per-scenario dimensions + the full turn distribution:
> [misc/DIVERSITY-COVERAGE-MATRIX.md](./misc/DIVERSITY-COVERAGE-MATRIX.md).

## Source selection and grounding

| ID | Scenario | Files selected | Turns | Main behavior | Diagram |
|---|---|---|---:|---|:--:|
| S001 | [Selected loops file, direct concept question](./scenarios/S001-selected-loops-file-direct-question.md) | php_loops | 12 | Grounds a while-vs-do…while answer and builds it into assessment | — |
| S002 | [No selected file, clear operators topic](./scenarios/S002-no-file-clear-operators-topic.md) | none | 12 | Auto-selects the operators deck and stays on it | — |
| S003 | [Wrong selected file conflicts with topic](./scenarios/S003-wrong-file-topic-conflict.md) | php_loops | 16 | Detects a mismatch, recovers, then builds correctly | — |
| S004 | [Two files for a structured comparison](./scenarios/S004-two-files-structured-comparison.md) | php_if_else, php_switch | 14 | Synthesizes if/elseif vs switch, iterates on the table | — |
| S005 | [All files: course revision guide](./scenarios/S005-all-files-revision-guide.md) | all 15 | 20 | Broad coverage + selective expansion + quiz | — |
| S006 | [Source changes during the conversation](./scenarios/S006-source-changes-midchat.md) | Module 1 → php_forms | 16 | Resolves "the second file" after a source switch | ✅ |
| S007 | [Explicit selection overrides source history](./scenarios/S007-explicit-selection-overrides-history.md) | php_arrays → php_strings | 14 | Current explicit source beats recent context | — |
| S008 | ["Use the same source" continuity](./scenarios/S008-use-same-source-continuity.md) | php_variables | 18 | Retains one source across many artifact types | ✅ |

## Natural teacher input and instruction styles

| ID | Scenario | Files selected | Turns | Main behavior | Diagram |
|---|---|---|---:|---|:--:|
| S009 | [Extremely short prompts](./scenarios/S009-extremely-short-prompt.md) | none | 10 | Recovers intent from minimal language, repeatedly | — |
| S010 | [Typo-heavy assessment prompts](./scenarios/S010-typo-heavy-assessment.md) | php_datatypes | 16 | Tolerates typos across a whole quiz workflow | — |
| S011 | [Conversational classroom problem](./scenarios/S011-conversational-classroom-problem.md) | none | 14 | Natural intent + pedagogical build-out | — |
| S012 | [Large instruction-heavy lesson request](./scenarios/S012-large-instruction-heavy-lesson.md) | Module 3 | 18 | Many constraints from one prompt, then refined | — |
| S013 | [Auditor adds one realistic instruction](./scenarios/S013-auditor-adds-one-instruction.md) | php_syntax | 12 | Honors an auditor-added constraint and continues | — |
| S014 | [Auditor writes the prompt](./scenarios/S014-auditor-writes-prompt.md) | Module 1 | 12 | Robust to realistic human wording | — |
| S015 | [Dense assessment constraints](./scenarios/S015-dense-assessment-constraints.md) | php_operators | 18 | Constraint compliance + targeted improvement | — |
| S016 | [Informal refinement language](./scenarios/S016-informal-refinement-language.md) | none | 14 | Informal edits preserve the definition | — |

## Ambiguity, clarification, contradiction, and recovery

| ID | Scenario | Files selected | Turns | Main behavior | Diagram |
|---|---|---|---:|---|:--:|
| S017 | [Referenced "Module 2" that does not exist](./scenarios/S017-missing-module-2.md) | none | 16 | Flags a missing/unsupported file rather than fabricating | ✅ |
| S018 | [Clear topic, indirect source name](./scenarios/S018-clear-topic-indirect-source.md) | none | 12 | Maps "the lecture about numbers" to the right file | — |
| S019 | ["Use these slides" with no active source](./scenarios/S019-use-these-slides-no-source.md) | none | 14 | Asks which slides; resolves the deictic reference | — |
| S020 | [Underspecified exam request](./scenarios/S020-underspecified-exam.md) | none | 18 | Clarifies efficiently, then builds and verifies | ✅ |
| S021 | [Directly conflicting item counts](./scenarios/S021-conflicting-item-counts.md) | none | 12 | Detects a contradiction, then completes cleanly | — |
| S022 | ["Same sources as before" in a new chat](./scenarios/S022-same-sources-new-chat.md) | none (new chat) | 12 | Doesn't invent context; recovers on selection | — |

## Course knowledge, explanation, and synthesis

| ID | Scenario | Files selected | Turns | Main behavior | Diagram |
|---|---|---|---:|---|:--:|
| S023 | [The 8 PHP data types](./scenarios/S023-php-data-types.md) | php_datatypes | 12 | Correctly lists the types, then builds | — |
| S024 | [GET vs POST](./scenarios/S024-get-vs-post.md) | php_forms | 14 | Comparison + in-framing application | — |
| S025 | [String functions (strlen / strpos)](./scenarios/S025-string-functions.md) | php_strings | 16 | Definitions → examples → student self-check | — |
| S026 | [PHP comment types](./scenarios/S026-php-comments.md) | php_comments | 12 | Distinguishes `//` `#` `/* */`, then assesses | — |
| S027 | [Form handling](./scenarios/S027-form-handling.md) | php_forms | 14 | action/method/name + `$_GET`/`$_POST` + security | — |
| S028 | [HTTP request/response synthesis](./scenarios/S028-http-synthesis.md) | Module 1 | 18 | Multi-step synthesis inside one source | — |

## Distinct artifact-generation workflows

| ID | Scenario | Files selected | Turns | Main behavior | Diagram |
|---|---|---|---:|---|:--:|
| S029 | [If/else quiz](./scenarios/S029-if-else-quiz.md) | php_if_else | 18 | Exactly ten Qs; reorder/refine without content loss | — |
| S030 | [Multi-file 20-point exam](./scenarios/S030-multi-file-20-point-exam.md) | php_loops, php_arrays, php_forms | 24 | Balanced multi-source exam; verify/replace/student | ✅ |
| S031 | [Arrays lesson plan](./scenarios/S031-arrays-lesson-plan.md) | php_arrays | 20 | Iterative lesson design into teaching assets | — |
| S032 | [Operators teaching slide deck](./scenarios/S032-operators-slide-deck.md) | php_operators | 20 | Slide-specific selective edits | — |
| S033 | [Student notes from PHP syntax](./scenarios/S033-student-notes-syntax.md) | php_syntax | 16 | Audience + length constraints; answer separation | — |
| S034 | [Forms + arrays assignment with rubric](./scenarios/S034-forms-arrays-assignment-rubric.md) | php_forms, php_arrays | 24 | Assignment + rubric continuity | — |

## Long multi-turn conversations

| ID | Scenario | Files selected | Turns | Main behavior | Diagram |
|---|---|---|---:|---|:--:|
| S035 | [Complete loops assessment lifecycle](./scenarios/S035-loops-assessment-lifecycle.md) | php_loops | 24 | Selective edits, count preservation, audience split | ✅ |
| S036 | [Strings lesson transformed into teaching assets](./scenarios/S036-strings-lesson-into-teaching-assets.md) | php_strings | 24 | One source → several connected artifacts | — |
| S037 | [Arrays quiz quality refinement](./scenarios/S037-arrays-quiz-quality-refinement.md) | php_arrays | 22 | Quality self-review + answer separation | — |
| S038 | [Source mismatch, correction, and recovery](./scenarios/S038-source-mismatch-correction-recovery.md) | php_strings → php_arrays | 20 | Graceful recovery after a source conflict | — |
| S039 | [Ambiguous exam via clarification and revision](./scenarios/S039-ambiguous-exam-clarification-revision.md) | none → php_if_else, php_switch, php_loops | 28 | Clarify, select, revise, verify totals | ✅ |
| S040 | [Complete mini course package](./scenarios/S040-complete-course-package-long-conversation.md) | Module 3, php_forms, php_arrays | 30 | Long-range multi-source, multi-artifact inventory | ✅ |
