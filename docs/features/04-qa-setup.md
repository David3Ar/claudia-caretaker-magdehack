# Feature 4 — QA / Setup

> Source: whiteboard photo IMG_2838 (not in repo). Priority: **M** (Primary #7 Web QA + #8 Setup, core cluster).
> Who: **C and G** both use it.

## Scope

- Entry: **talk to agent**
- Outcomes:
  - Document in diary
  - Add to calendar
  - Research in web
  - Change config

## Structure

```mermaid
flowchart TD
    T["🗣 Talk to agent<br/>(C or G)"]:::core
    T --> D[Document in diary]
    T --> CAL[Add to calendar]
    T --> W[Research in web]
    T --> CFG[Change config]
    D -.-> CFG
    W -.-> CFG

    classDef core fill:#e8590c,stroke:#e8590c,color:#fff
```

## Intent routing

```mermaid
flowchart LR
    U(["C / G utterance"]) --> I{Intent}
    I -->|memory / note| D[(Diary)]
    I -->|date / event| CAL[(Calendar)]
    I -->|question| WEB[Web QA]
    I -->|preference / setting| CFG[(Config)]
    WEB --> R([Voice answer])
```

## Open points

- [ ] Arrows diary/web → change config on board: meaning **to be discussed**
- [ ] Which config is voice-changeable, and by whom (C vs. G rights)
- [ ] Web QA sources / safety filtering
- [ ] "Setup" onboarding flow itself not drawn
