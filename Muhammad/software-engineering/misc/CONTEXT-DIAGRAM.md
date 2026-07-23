# Context Diagram and Audit Workflow

How a scenario becomes a result. Read this once so the scenario files stay short.

## Main context

```mermaid
flowchart LR
    A[Scenario .md] --> B[Human Auditor]
    B -->|Select files| C[Fazah Course]
    B -->|Enter prompts| D[Fazah Chat]
    C --> D
    D --> E[Course Materials]
    E --> D
    D -->|Answer or artifact| B
    B --> F[Audit Result]
    B --> G[Evidence]
    F --> H[Metrics and Review]
    G --> H
    H --> I[Fix and Retest]
```

## Auditor workflow

```mermaid
flowchart TD
    A[Open scenario] --> B[Set up files]
    B --> C[Enter prompt]
    C --> D[Wait for response]
    D --> E[Check expectations]
    E --> F{More turns?}
    F -->|Yes| C
    F -->|No| G[Mark result]
    G --> H[Add one note]
    H --> I[Save evidence]
```

## Multi-turn context

```mermaid
flowchart LR
    A[Create] --> B[Remember sources and artifact]
    B --> C[Edit]
    C --> D[Preserve unchanged content]
    D --> E[Refine]
    E --> F[Keep previous edits]
    F --> G[Final student or teacher version]
```

## Expected versus actual

```mermaid
flowchart LR
    A[Scenario expectation] --> C{Compare}
    B[Fazah behavior] --> C
    C -->|Correct| D[Pass]
    C -->|Minor issue| E[Small issue]
    C -->|Important problem| F[Fail]
    C -->|Fabrication or leakage| G[Critical fail]
```

## Scenario-specific diagrams

Eight scenarios carry their own small (≤6-node) workflow diagram because their source/turn flow is
the thing under test. All other 32 scenarios have no diagram — follow the turns in order.

| Scenario | Why it has a diagram |
|---|---|
| S006 | Source changes mid-chat; the switch is the test |
| S008 | "Use the same source" chained across artifact types |
| S017 | Chapter-number ambiguity → clarify → proceed |
| S020 | Underspecified exam built through minimal clarification |
| S030 | Multi-file exam with verify/replace/student-version branch |
| S035 | Eight-turn assessment lifecycle with selective edits |
| S039 | Ambiguous exam built through clarification and revision |
| S040 | Mini-course package: multi-source, multi-artifact inventory |
