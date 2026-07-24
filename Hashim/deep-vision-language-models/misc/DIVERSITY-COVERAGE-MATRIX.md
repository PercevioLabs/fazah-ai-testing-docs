# Diversity Coverage Matrix — AI623 DVLM Suite

One row per scenario. This is the master plan that guarantees every scenario is **materially
different** — no two rows share the same full combination of
(Turns × Teacher style × Prompt size × Source state × Task type × Audience × Main risk).

**Every scenario is a multi-turn conversation (6–16 turns)** on one continuous teacher goal.
"Prompt size" describes the typical turn prompt. **Risk vocabulary** aligns with the
Critical-fail triggers in [AUDITOR-INSTRUCTIONS](../AUDITOR-INSTRUCTIONS.md): Ambiguity,
Unsupported request, Fabrication, Grounding drift, Instruction loss, Contradiction,
Count/marks integrity, Answer leakage, Work destruction, Unreadable source.

| ID | Turns | Teacher style | Prompt size | Source state | Task type | Audience | Main risk |
|---|---:|---|---|---|---|---|---|
| S001 | 6 | Direct | Short | 1 selected | Q&A → quiz | Teacher | Grounding drift |
| S002 | 6 | Direct | Short | none (clear topic) | Q&A → quiz | Teacher | Wrong auto-selection |
| S003 | 8 | Direct | Medium | wrong file selected | Q&A recovery | Teacher | Grounding drift |
| S004 | 7 | Structured | Medium | 2 selected | Comparison table | Teacher | Fabrication |
| S005 | 9 | Planning | Medium | all selected | Revision guide + quiz | Students | Coverage gaps |
| S006 | 8 | Direct | Short | switch mid-chat | Q&A continuity | Teacher | Reference resolution |
| S007 | 7 | Direct | Short | history vs explicit | Q&A | Teacher | Selection precedence |
| S008 | 9 | Direct | Short | 1 sticky source | Quiz → notes → summary | Mixed | Source continuity |
| S009 | 6 | Terse | Tiny | none | Q&A → quiz | Teacher | Intent recovery |
| S010 | 8 | Typo-heavy | Short | 1 selected | Quiz workflow | Students | Robust parsing |
| S011 | 7 | Conversational | Medium | none | Lesson advice | Teacher | Pedagogy quality |
| S012 | 8 | Instruction-heavy | Long | 1 selected | Lesson plan | Students | Instruction loss |
| S013 | 6 | Direct + auditor add | Short | 1 selected | Notes | Students | Constraint adherence |
| S014 | 6 | Auditor-written | Medium | 1 selected | Q&A → artifact | Teacher | Natural wording |
| S015 | 9 | Precise counts | Long | 1 selected | Assessment | Students | Count/marks integrity |
| S016 | 7 | Informal slang | Short | none | Quiz refinement | Students | Definition preservation |
| S017 | 8 | Direct | Short | ambiguous + unreadable | Source resolution | Teacher | Unreadable source honesty |
| S018 | 6 | Indirect | Short | none | Source mapping | Teacher | Ambiguity |
| S019 | 7 | Deictic | Short | none | Quiz | Students | Clarification quality |
| S020 | 9 | Vague | Short→Long | none → multi | Exam build | Students | Under-specification |
| S021 | 6 | Contradictory | Medium | none | Quiz | Students | Contradiction detection |
| S022 | 6 | Assumes context | Short | new chat, none | Continuity recovery | Teacher | Invented context |
| S023 | 6 | Direct | Short | 1 selected | Definitions + exercise | Students | Definition fidelity |
| S024 | 7 | Direct | Medium | 1 selected | Concept chain | Students | Formula fidelity |
| S025 | 8 | Direct | Medium | 1 selected | Concept + assessment | Mixed | Formula fidelity |
| S026 | 6 | Direct | Short | 1 selected | Comparison + questions | Teacher | Technical precision |
| S027 | 7 | Direct | Medium | 1 selected | Concept chain | Teacher | Formula fidelity |
| S028 | 9 | Synthesis | Medium | 3 selected | Synthesis table + quiz | Mixed | Multi-source balance |
| S029 | 9 | Precise counts | Medium | 2 selected | 10-question quiz | Students | Count integrity |
| S030 | 12 | Structured | Medium | 3 selected | 20-point exam | Students | Marks integrity + leakage |
| S031 | 10 | Planning | Medium | 2 selected | Lesson plan → assets | Students | Cross-artifact consistency |
| S032 | 10 | Selective edits | Medium | 1 selected | Slide deck | Students | Targeted edits only |
| S033 | 8 | Constraint-driven | Medium | 1 selected | Student notes | Students | Audience + length |
| S034 | 12 | Structured | Medium | 2 selected | Assignment + rubric | Students | Rubric consistency |
| S035 | 12 | Lifecycle | Mixed | 1 selected | Assessment lifecycle | Mixed | Work destruction |
| S036 | 12 | Lifecycle | Mixed | 1 selected | Plan → assets | Students | Cross-artifact consistency |
| S037 | 11 | Quality-focused | Medium | 1 selected | Numeric quiz + delivery | Students | Arithmetic + leakage |
| S038 | 10 | Direct | Medium | wrong → right | Recovery workflow | Teacher | Mismatch recovery |
| S039 | 14 | Vague → precise | Mixed | none → 3 | Exam via clarification | Students | Totals verification |
| S040 | 16 | Marathon | Mixed | 3 selected | Full course package | Mixed | Long-range consistency |
