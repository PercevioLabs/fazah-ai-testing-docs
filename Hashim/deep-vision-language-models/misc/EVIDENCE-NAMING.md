# Evidence Naming

Name every screenshot, export, or saved response so anyone can trace it back to a scenario, turn,
and auditor without opening it.

## Pattern

```text
<batch>-<scenario>-<auditor>-turn-<number>-<evidence-type>.<ext>
```

- **batch** — the audit batch id, e.g. `A01` (see `audit_batch` in the CSVs).
- **scenario** — the scenario id, e.g. `S035`.
- **auditor** — short lowercase name/handle, e.g. `usama`, `sarah`.
- **number** — the turn number the evidence belongs to (`1`, `2`, …). Use `final` for whole-scenario
  evidence that isn't tied to one turn.
- **evidence-type** — short kebab-case label of what it shows (see list below).
- **ext** — `png`, `jpg`, `pdf`, `docx`, `pptx`, `txt`, `md`, …

## Examples

```text
A01-S035-usama-turn-1-response.png
A01-S035-usama-turn-7-student-version.pdf
A01-S038-sarah-turn-2-source-warning.png
A01-S030-sarah-turn-5-teacher-key.pdf
A01-S017-omar-turn-1-clarification.png
A01-S004-lena-turn-1-comparison-table.png
A01-S040-usama-final-artifact-inventory.md
```

## Common evidence-type labels

| Label | Use for |
|---|---|
| `response` | The chat reply text |
| `sources-used` | The "Sources used (N)" panel on an artifact |
| `used-sources` | The reply-level "Used sources" / Sources disclosure |
| `grounded-badge` | The "Grounded in your course materials" badge |
| `source-warning` | A note that the selected file doesn't support the request |
| `clarification` | A clarifying question or stated safe assumption |
| `student-version` | Student-facing artifact (verify no answers) |
| `teacher-key` | Teacher version / answer key |
| `artifact` | A generated quiz/exam/lesson/slides/notes/etc. |
| `version-diff` | Before/after of an edited artifact version |
| `files-selected` | The Course Files / Sources panel showing selection |
| `error` | An error, timeout, or broken state |

## Tips

- One file = one clear thing. Prefer several small screenshots over one crowded one.
- For edit turns, capture **both** the before and after (`version-diff`) so "only the requested
  thing changed" is verifiable.
- Put the evidence link in the `evidence_link` column of the CSV row for that turn.
