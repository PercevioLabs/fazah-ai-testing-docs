# Scenario Index

All 40 scenarios, grouped by category. Every scenario is a **multi-turn teacher conversation**
(6–16 turns) on one continuous goal — a real teacher rarely stops after one message. "Files
selected" is the starting selection (some scenarios change or add files mid-chat — see the
scenario). "Workflow diagram" marks the eight scenarios that carry a small scenario-specific diagram.

> Turn spread: min 6, max 16, average ~8 turns. See the per-scenario dimensions in
> [DIVERSITY-COVERAGE-MATRIX.md](./misc/DIVERSITY-COVERAGE-MATRIX.md).

## Source selection and grounding

| ID | Scenario | Category | Files selected | Turns | Main behavior | Workflow diagram |
|---|---|---|---|---:|---|:--:|
| S001 | [Selected Testing file, direct concept question](./scenarios/S001-selected-testing-file-direct-question.md) | Source selection | Ch4 Testing | 6 | Grounds a V&V thread and builds it into assessment | — |
| S002 | [No selected file, clear testing topic](./scenarios/S002-no-file-clear-topic.md) | Source selection | none | 6 | Auto-selects the right source and stays on it | — |
| S003 | [Wrong selected file conflicts with topic](./scenarios/S003-wrong-file-topic-conflict.md) | Source selection | Ch5 Agile | 8 | Detects a mismatch, recovers, then builds correctly | — |
| S004 | [Two files for a structured comparison](./scenarios/S004-two-files-structured-comparison.md) | Source selection | Ch2 Processes, Ch5 Agile | 7 | Synthesizes two sources and iterates on the table | — |
| S005 | [All files: course revision guide](./scenarios/S005-all-files-revision-guide.md) | Source selection | all five | 9 | Broad coverage + selective expansion + quiz | — |
| S006 | [Source changes during the conversation](./scenarios/S006-source-changes-midchat.md) | Source selection | Ch3 → Ch4 | 8 | Resolves "the second file" after a source switch | ✅ |
| S007 | [Explicit selection overrides source history](./scenarios/S007-explicit-selection-overrides-history.md) | Source selection | Ch5 → Ch4 | 7 | Current explicit source beats recent context | — |
| S008 | ["Use the same source" continuity](./scenarios/S008-use-same-source-continuity.md) | Source selection | Ch4 Testing | 9 | Retains one source across many artifact types | ✅ |

## Natural teacher input and instruction styles

| ID | Scenario | Category | Files selected | Turns | Main behavior | Workflow diagram |
|---|---|---|---|---:|---|:--:|
| S009 | [Extremely short prompts](./scenarios/S009-extremely-short-prompt.md) | Natural input | none | 6 | Recovers intent from minimal language, repeatedly | — |
| S010 | [Typo-heavy assessment prompts](./scenarios/S010-typo-heavy-assessment.md) | Natural input | Ch4 Testing | 8 | Tolerates typos across a whole quiz workflow | — |
| S011 | [Conversational classroom problem](./scenarios/S011-conversational-classroom-problem.md) | Natural input | none | 7 | Natural intent + pedagogical build-out | — |
| S012 | [Large instruction-heavy lesson request](./scenarios/S012-large-instruction-heavy-lesson.md) | Natural input | Ch5 Agile | 8 | Many constraints from one prompt, then refined | — |
| S013 | [Auditor adds one realistic instruction](./scenarios/S013-auditor-adds-one-instruction.md) | Natural input | Ch1 Introduction | 6 | Honors an auditor-added constraint and continues | — |
| S014 | [Auditor writes the prompt](./scenarios/S014-auditor-writes-prompt.md) | Natural input | Ch5 Agile | 6 | Robust to realistic human wording | — |
| S015 | [Dense assessment constraints](./scenarios/S015-dense-assessment-constraints.md) | Natural input | Ch4 Testing | 9 | Constraint compliance + targeted improvement | — |
| S016 | [Informal refinement language](./scenarios/S016-informal-refinement-language.md) | Natural input | none | 7 | Informal edits preserve the definition | — |

## Ambiguity, clarification, contradiction, and recovery

| ID | Scenario | Category | Files selected | Turns | Main behavior | Workflow diagram |
|---|---|---|---|---:|---|:--:|
| S017 | [Ambiguous "Chapter 4"](./scenarios/S017-ambiguous-chapter-4.md) | Ambiguity & recovery | none | 8 | Resolves filename-vs-internal chapter ambiguity | ✅ |
| S018 | [Clear topic, indirect source name](./scenarios/S018-clear-topic-indirect-source.md) | Ambiguity & recovery | none | 6 | Maps "the chapter about testing" to the right file | — |
| S019 | ["Use these slides" with no active source](./scenarios/S019-use-these-slides-no-source.md) | Ambiguity & recovery | none | 7 | Asks which slides; resolves the deictic reference | — |
| S020 | [Underspecified exam request](./scenarios/S020-underspecified-exam.md) | Ambiguity & recovery | none | 9 | Clarifies efficiently, then builds and verifies | ✅ |
| S021 | [Directly conflicting item counts](./scenarios/S021-conflicting-item-counts.md) | Ambiguity & recovery | none | 6 | Detects a contradiction, then completes cleanly | — |
| S022 | ["Same sources as before" in a new chat](./scenarios/S022-same-sources-new-chat.md) | Ambiguity & recovery | none (new chat) | 6 | Doesn't invent context; recovers on selection | — |

## Course knowledge, explanation, and synthesis

| ID | Scenario | Category | Files selected | Turns | Main behavior | Workflow diagram |
|---|---|---|---|---:|---|:--:|
| S023 | [Attributes of good software](./scenarios/S023-attributes-of-good-software.md) | Course knowledge | Ch1 Introduction | 6 | Correctly lists the four attributes, then builds | — |
| S024 | [Waterfall vs incremental development](./scenarios/S024-waterfall-vs-incremental.md) | Course knowledge | Ch2 Processes | 7 | Comparison + in-framing application | — |
| S025 | [Functional vs non-functional requirements](./scenarios/S025-functional-vs-nonfunctional.md) | Course knowledge | Ch3 Req Eng | 8 | Definitions → Mentcare example → student self-check | — |
| S026 | [Verification, validation, inspections, testing](./scenarios/S026-verification-validation-inspections-testing.md) | Course knowledge | Ch4 Testing | 6 | Distinguishes all four concepts, then assesses | — |
| S027 | [Testing levels and interface faults](./scenarios/S027-testing-levels-interface-faults.md) | Course knowledge | Ch4 Testing | 7 | Levels + interface-error examples, then questions | — |
| S028 | [Agile Manifesto, XP, and Scrum synthesis](./scenarios/S028-agile-manifesto-xp-scrum-synthesis.md) | Course knowledge | Ch5 Agile | 9 | Multi-step synthesis inside one source | — |

## Distinct artifact-generation workflows

| ID | Scenario | Category | Files selected | Turns | Main behavior | Workflow diagram |
|---|---|---|---|---:|---|:--:|
| S029 | [Ten-question Testing quiz](./scenarios/S029-ten-question-testing-quiz.md) | Artifact generation | Ch4 Testing | 9 | Exactly ten Qs; reorder/refine without content loss | — |
| S030 | [Multi-file 20-point exam](./scenarios/S030-multi-file-20-point-exam.md) | Artifact generation | Ch2, Ch3, Ch4 | 12 | Balanced multi-source exam; verify/replace/student | ✅ |
| S031 | [Agile lesson plan](./scenarios/S031-agile-lesson-plan.md) | Artifact generation | Ch5 Agile | 10 | Iterative lesson design into teaching assets | — |
| S032 | [Requirements teaching slide deck](./scenarios/S032-requirements-slide-deck.md) | Artifact generation | Ch3 Req Eng | 10 | Slide-specific selective edits | — |
| S033 | [Student notes from Introduction](./scenarios/S033-student-notes-introduction.md) | Artifact generation | Ch1 Introduction | 8 | Audience + length constraints; answer separation | — |
| S034 | [Comparison assignment with rubric](./scenarios/S034-comparison-assignment-rubric.md) | Artifact generation | Ch2 Processes, Ch5 Agile | 12 | Assignment + rubric continuity | — |

## Long multi-turn conversations

| ID | Scenario | Category | Files selected | Turns | Main behavior | Workflow diagram |
|---|---|---|---|---:|---|:--:|
| S035 | [Complete Requirements assessment lifecycle](./scenarios/S035-requirements-assessment-lifecycle.md) | Long workflow | Ch3 Req Eng | 12 | Selective edits, count preservation, audience split | ✅ |
| S036 | [Lesson plan transformed into teaching assets](./scenarios/S036-lesson-plan-into-teaching-assets.md) | Long workflow | Ch2 Processes | 12 | One source → several connected artifacts | — |
| S037 | [Quiz quality refinement and student delivery](./scenarios/S037-quiz-quality-refinement.md) | Long workflow | Ch4 Testing | 11 | Quality self-review + answer separation | — |
| S038 | [Source mismatch, correction, and recovery](./scenarios/S038-source-mismatch-correction-recovery.md) | Long workflow | Ch5 → Ch3 | 10 | Graceful recovery after a source conflict | — |
| S039 | [Ambiguous exam via clarification and revision](./scenarios/S039-ambiguous-exam-clarification-revision.md) | Long workflow | none → Ch2, Ch3, Ch4 | 14 | Clarify, select, revise, verify totals | ✅ |
| S040 | [Complete mini course package](./scenarios/S040-complete-course-package-long-conversation.md) | Long workflow | Ch1, Ch2, Ch5 | 16 | Long-range multi-source, multi-artifact inventory | ✅ |
