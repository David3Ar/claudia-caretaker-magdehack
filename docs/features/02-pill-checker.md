# Feature 2 — Pill Checker

> Source: whiteboard photo IMG_2836 (not in repo). Priority: **M** (Primary #3, core ✔).

## Scope

- Works with **calendar** (intake times = events)
- **Setup:** from picture → plan → config
- **Intake check — how?**
  - Camera + detection → phone or device (camera / sensor)
  - Just ask (voice confirmation)
- **Scheduled agent asks** → document in diary
- **Not home?** → response + document
- **Forgot?** → raise attention → report (health status)
- **Quick help** (content **open**)

## Structure

```mermaid
mindmap
  root((Pill Checker))
    Setup
      Picture of prescription
      Plan
      Config
    Check method
      Camera + detection
        Phone
        Device
          Camera
          Sensor
      Just ask
    Calendar link
      Not home → response + document
    Escalation
      Forgot → raise attention
      Report / health status
    Quick help ?
```

## Flow — daily intake

```mermaid
flowchart TD
    P["Picture → plan → config"]:::setup --> CAL[(Calendar)]
    CAL -->|intake time| ASK{Agent asks G}
    ASK -->|taken| DOC["Document in diary"]:::ok
    ASK -->|not home| NH["Response + document"]
    ASK -->|no answer / forgot| RA["Raise attention"]:::alert
    RA --> REP["Report → C<br/>health status"]:::alert
    ASK -.->|optional| CAM["Camera / sensor<br/>verification"]

    classDef setup fill:#1e3a5f,stroke:#1e3a5f,color:#fff
    classDef ok fill:#2b8a3e,stroke:#2b8a3e,color:#fff
    classDef alert fill:#e03131,stroke:#e03131,color:#fff
```

## Open points

- [ ] Verification method for demo: camera vs. "just ask"
- [ ] "Quick help" — what exactly?
- [ ] Escalation thresholds (retries, delay before alert)
- [ ] "Not home" — how detected (location? answer?)
- [ ] Pill box w/ sensors = tertiary (C) — out of demo scope?
