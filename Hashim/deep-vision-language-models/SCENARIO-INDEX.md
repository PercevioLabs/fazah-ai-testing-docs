# Scenario Index — AI623 Deep Vision Language Models

All 40 scenarios, grouped by category. Every scenario is a **multi-turn teacher conversation**
(6–16 turns) on one continuous goal. "Files selected" is the starting selection (some scenarios
change or add files mid-chat — see the scenario). File numbers refer to the
[COURSE-CONTENT-MAP](./COURSE-CONTENT-MAP.md).

> Turn spread: min 6, max 16, average ~8.5 turns.

## Source selection and grounding

| ID | Scenario | Category | Files selected | Turns | Main behavior |
|---|---|---|---|---:|---|
| S001 | [Selected diffusion notes, direct concept question](./scenarios/S001-selected-diffusion-notes-direct-question.md) | Source selection | 06 diffusion | 6 | Grounds a DDPM/DDIM thread and builds it into assessment |
| S002 | [No selected file, clear flow-matching topic](./scenarios/S002-no-file-clear-topic.md) | Source selection | none | 6 | Auto-selects the right source and stays on it |
| S003 | [Wrong selected file conflicts with topic](./scenarios/S003-wrong-file-topic-conflict.md) | Source selection | 04 VAE | 8 | Asks about GRPO with VAE notes selected; detects mismatch, recovers |
| S004 | [Two files for a structured comparison](./scenarios/S004-two-files-structured-comparison.md) | Source selection | 05 NCSN, 06 diffusion | 7 | Synthesizes NCSN vs DDPM and iterates on the table |
| S005 | [All files: course revision guide](./scenarios/S005-all-files-revision-guide.md) | Source selection | all | 9 | Broad coverage + selective expansion + quiz |
| S006 | [Source changes during the conversation](./scenarios/S006-source-changes-midchat.md) | Source selection | 04 → 06 | 8 | Resolves references cleanly after a source switch |
| S007 | [Explicit selection overrides source history](./scenarios/S007-explicit-selection-overrides-history.md) | Source selection | 09 → 12 | 7 | Current explicit source beats recent context |
| S008 | ["Use the same source" continuity](./scenarios/S008-use-same-source-continuity.md) | Source selection | 12 VLM | 9 | Retains one source across many artifact types |

## Natural teacher input and instruction styles

| ID | Scenario | Category | Files selected | Turns | Main behavior |
|---|---|---|---|---:|---|
| S009 | [Extremely short prompts](./scenarios/S009-extremely-short-prompt.md) | Natural input | none | 6 | Recovers intent from "ddim?", "eta?", "quiz" |
| S010 | [Typo-heavy assessment prompts](./scenarios/S010-typo-heavy-assessment.md) | Natural input | 06 diffusion | 8 | Tolerates typos across a whole quiz workflow |
| S011 | [Conversational classroom problem](./scenarios/S011-conversational-classroom-problem.md) | Natural input | none | 7 | "Students confuse score matching with plain denoising" → pedagogical build-out |
| S012 | [Large instruction-heavy lesson request](./scenarios/S012-large-instruction-heavy-lesson.md) | Natural input | 07 flow matching | 8 | Many constraints from one prompt, then refined |
| S013 | [Auditor adds one realistic instruction](./scenarios/S013-auditor-adds-one-instruction.md) | Natural input | 01 intro | 6 | Honors an auditor-added constraint and continues |
| S014 | [Auditor writes the prompt](./scenarios/S014-auditor-writes-prompt.md) | Natural input | 09 alignment | 6 | Robust to realistic human wording |
| S015 | [Dense assessment constraints](./scenarios/S015-dense-assessment-constraints.md) | Natural input | 04 VAE | 9 | Exact counts, types, marks honored, then targeted improvement |
| S016 | [Informal refinement language](./scenarios/S016-informal-refinement-language.md) | Natural input | none | 7 | "make q2 spicier" / "nah, chill it" edits preserve definitions |

## Ambiguity, clarification, contradiction, and recovery

| ID | Scenario | Category | Files selected | Turns | Main behavior |
|---|---|---|---|---:|---|
| S017 | [Ambiguous "lecture 2" + unreadable handwritten file](./scenarios/S017-ambiguous-lecture-2-handwritten.md) | Ambiguity & recovery | none | 8 | Filename ambiguity plus a source with no extractable text — honesty check |
| S018 | [Clear topic, indirect source name](./scenarios/S018-clear-topic-indirect-source.md) | Ambiguity & recovery | none | 6 | "the notes about the sampler that removes randomness" → DDIM file |
| S019 | ["Use these slides" with no active source](./scenarios/S019-use-these-slides-no-source.md) | Ambiguity & recovery | none | 7 | Asks which slides; resolves the deictic reference |
| S020 | [Underspecified exam request](./scenarios/S020-underspecified-exam.md) | Ambiguity & recovery | none | 9 | Clarifies efficiently, then builds and verifies |
| S021 | [Directly conflicting item counts](./scenarios/S021-conflicting-item-counts.md) | Ambiguity & recovery | none | 6 | Detects a contradiction, then completes cleanly |
| S022 | ["Same sources as before" in a new chat](./scenarios/S022-same-sources-new-chat.md) | Ambiguity & recovery | none (new chat) | 6 | Doesn't invent context; recovers on selection |

## Course knowledge, explanation, and synthesis

| ID | Scenario | Category | Files selected | Turns | Main behavior |
|---|---|---|---|---:|---|
| S023 | [LLM vs VLM vs MLLM definitions](./scenarios/S023-llm-vlm-mllm-definitions.md) | Course knowledge | 01 intro | 6 | Correct intro-deck definitions, then builds on them |
| S024 | [DAE, Tweedie, and the reparameterization trick](./scenarios/S024-dae-tweedie-reparameterization.md) | Course knowledge | 04 VAE | 7 | Definitions → formulas → student self-check |
| S025 | [Score ↔ noise, Langevin dynamics](./scenarios/S025-score-noise-langevin.md) | Course knowledge | 05 NCSN | 8 | True score, NCSN loss, annealed Langevin, then assesses |
| S026 | [DDPM vs DDIM and the η parameter](./scenarios/S026-ddpm-vs-ddim-eta.md) | Course knowledge | 06 diffusion | 6 | Distinguishes samplers; η=0 determinism, then questions |
| S027 | [VE vs VP SDEs and predictor–corrector](./scenarios/S027-ve-vp-sde-predictor-corrector.md) | Course knowledge | 07 flow matching | 7 | Drift/diffusion identification + sampler structure |
| S028 | [PPO vs DPO vs GRPO synthesis](./scenarios/S028-ppo-dpo-grpo-synthesis.md) | Course knowledge | 09, 10, 11 | 9 | Multi-file synthesis of the alignment pipeline |

## Distinct artifact-generation workflows

| ID | Scenario | Category | Files selected | Turns | Main behavior |
|---|---|---|---|---:|---|
| S029 | [Ten-question diffusion quiz](./scenarios/S029-ten-question-diffusion-quiz.md) | Artifact generation | 06, 08 | 9 | Exactly ten Qs; reorder/refine without content loss |
| S030 | [Multi-file 20-point generative-models exam](./scenarios/S030-multi-file-20-point-exam.md) | Artifact generation | 05, 06, 07 | 12 | Balanced multi-source exam; verify/replace/student copy |
| S031 | [Alignment lesson plan](./scenarios/S031-alignment-lesson-plan.md) | Artifact generation | 09, 11 | 10 | Iterative lesson design into teaching assets |
| S032 | [VLM teaching slide deck](./scenarios/S032-vlm-slide-deck.md) | Artifact generation | 12 VLM | 10 | Slide-specific selective edits |
| S033 | [Student notes from the intro deck](./scenarios/S033-student-notes-introduction.md) | Artifact generation | 01 intro | 8 | Audience + length constraints; answer separation |
| S034 | [Comparison assignment with rubric](./scenarios/S034-comparison-assignment-rubric.md) | Artifact generation | 05, 07 | 12 | NCSN-vs-flow-matching assignment + rubric continuity |

## Long multi-turn conversations

| ID | Scenario | Category | Files selected | Turns | Main behavior |
|---|---|---|---|---:|---|
| S035 | [Complete VAE assessment lifecycle](./scenarios/S035-vae-assessment-lifecycle.md) | Long workflow | 04 VAE | 12 | Selective edits, count preservation, audience split |
| S036 | [Lesson plan transformed into teaching assets](./scenarios/S036-lesson-plan-into-teaching-assets.md) | Long workflow | 06 diffusion | 12 | One source → several connected artifacts |
| S037 | [Quiz quality refinement and student delivery](./scenarios/S037-quiz-quality-refinement.md) | Long workflow | 10 worked problems | 11 | Numeric-answer verification + answer separation |
| S038 | [Source mismatch, correction, and recovery](./scenarios/S038-source-mismatch-correction-recovery.md) | Long workflow | 11 → 12 | 10 | Graceful recovery after a source conflict |
| S039 | [Ambiguous exam via clarification and revision](./scenarios/S039-ambiguous-exam-clarification-revision.md) | Long workflow | none → 05, 06, 07 | 14 | Clarify, select, revise, verify totals |
| S040 | [Complete mini course package](./scenarios/S040-complete-course-package-long-conversation.md) | Long workflow | 01, 06, 09 | 16 | Long-range multi-source, multi-artifact inventory |
