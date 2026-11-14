# Feature 3 — Live Location + Emergency Alert

> Source: `todo/IMG_2837`. Priority: **M** (Primary #6 + #9; core cluster incl. messaging).

## Scope

1. **C sees G** — caregiver sees senior's location
2. **(G sees C)** — in brackets on board → lower priority / **open**
   - "Where is my son?"
   - "Ask him to call me"
3. **Emergency alert** — triggers:
   - Not responding → take action
   - Smart watch
   - Button

## Structure

```mermaid
flowchart LR
    LL[Live Location]:::core
    LL --> CG["1 · C sees G"]
    LL --> GC["2 · G sees C ?"]
    GC --> Q1["'Where is my son?'"]
    GC --> Q2["'Ask him to call me'"]
    LL --> EM[3 · Emergency Alert]:::alert
    EM --> T1[Not responding]
    EM --> T2[Smart watch]
    EM --> T3[Button]
    T1 --> ACT((Take action)):::alert
    T2 --> ACT
    T3 --> ACT

    classDef core fill:#e8590c,stroke:#e8590c,color:#fff
    classDef alert fill:#e03131,stroke:#e03131,color:#fff
```

## Flow — "Where is my son?"

```mermaid
sequenceDiagram
    actor G as Senior
    participant A as Voice Agent
    actor C as Caregiver
    G->>A: "Where is my son?"
    A->>A: read C location (if shared)
    A-->>G: location info (format open)
    G->>A: "Ask him to call me"
    A->>C: push: call request
    C-->>G: call
```

## Open points

- [ ] "Take action" — what action? (call C, call emergency services, escalation chain)
- [ ] Privacy / consent for G sees C
- [ ] Smart watch = tertiary (C) — demo with button only?
- [ ] Messaging part of this cluster — scope undefined
