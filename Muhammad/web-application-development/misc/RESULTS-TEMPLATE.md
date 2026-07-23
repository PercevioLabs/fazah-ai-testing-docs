# Results Template

Copy this file per audit batch (e.g. `RESULTS-A01.md`) and fill the tables. Keep notes to one line.
Result values: `Pass` / `Pass with small issue` / `Fail` / `Critical fail`. Sub-columns use
`Yes / Mostly / Partly / No / N/A` as appropriate (see each scenario's Final Check).

## Scenario results

| Scenario | Auditor | Prompt entered | Files selected | Overall result | Understanding | Source use | Output quality | Conversation | Main issue | Evidence | Note |
|---|---|---|---|---|---|---|---|---|---|---|---|
| S001 |  |  |  |  |  |  |  |  |  |  |  |
| S002 |  |  |  |  |  |  |  |  |  |  |  |
| S003 |  |  |  |  |  |  |  |  |  |  |  |
| S004 |  |  |  |  |  |  |  |  |  |  |  |
| S005 |  |  |  |  |  |  |  |  |  |  |  |
| … |  |  |  |  |  |  |  |  |  |  |  |
| S040 |  |  |  |  |  |  |  |  |  |  |  |

> Add one row per scenario you ran (S001–S040). Every scenario is multi-turn (6–16 turns), so
> `Conversation` always applies — judge whether context was held across the whole conversation.

## Turn-level results (multi-turn scenarios)

| Scenario | Turn | Prompt | Expected change | Actual change | Result | Note |
|---|---:|---|---|---|---|---|
| S035 | 1 |  |  |  |  |  |
| S035 | 2 |  |  |  |  |  |
| S035 | … |  |  |  |  |  |
| S040 | 8 |  |  |  |  |  |

> For every edit turn, `Expected change` vs `Actual change` must make clear whether **only** the
> requested content changed. Any unrequested change is at least a Fail (Critical if it destroyed work).
