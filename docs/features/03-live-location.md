# Feature 3 — Live Location + Emergency Alert

> `C` = caregiver · `G` = senior

## Scope

- **Hands-free:** wake word "Hey Claudia" starts every conversation; after that `G` only talks
- **C sees G:** place name, map, today's places; normal movement sends no push
- **G sees C** (lower priority, consent **open**):
  - "Where is my son?" → coarse answer ("at work")
  - "Ask him to call me" → call request to `C`
  - "Call Jonas" → direct call, no question back
- **Emergency alert** → full-screen alert to every `C`, with location
  - "Hey Claudia, help!"
  - Button (fallback)
  - Not responding → amber, then coral
  - Smart watch (Could)
- "Take action" after an alert → **open**

## Structure

```mermaid
flowchart TD
    LL[Live Location]:::core
    LL --> HF["Hands-free<br/>Hey Claudia"]
    LL --> CG["C sees G<br/>place, map, history"]
    LL --> GC["G sees C<br/>coarse place"]
    GC --> CR["Call request"]
    GC --> DC["Direct call"]
    LL --> EM[Emergency Alert]:::alert
    EM --> T1["Voice: help"]
    EM --> T2[Button]
    EM --> T3[Not responding]
    EM --> T4[Smart watch]
    T1 --> ACT((Take action)):::alert
    T2 --> ACT
    T3 --> ACT
    T4 --> ACT

    classDef core fill:#e8590c,stroke:#e8590c,color:#fff
    classDef alert fill:#e03131,stroke:#e03131,color:#fff
```

Spec, requirements and flows: [`specs/03-live-location/spec.md`](../specs/03-live-location/spec.md)
