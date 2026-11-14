# Feature 1 — Calendar / Scheduling

> `C` = caregiver · `G` = senior

## Scope

- Internal calendar
- Events creatable by **C and G**
- Sync with personal calendar (C's external calendar — provider **open**)
- Actions on scheduled tasks:
  - `Ask` → Document (agent asks G a predefined question, logs answer in Diary)
  - `Stock reminder` → initiate ordering
- Availability check → shift appointment or assign appointment responsible C → reminders for C and G (configurable in calendar)

## Structure





```mermaid
flowchart TD
    CAL[Internal Calendar]:::core
    CAL --> EV["Create events<br/>by C + G"]
    EV --> SYNC["Sync with<br/>personal calendar"]
    CAL --> TS[Task Scheduler]
    TS --> AD["Ask → document"]
    TS --> SR["Stack reminders<br/>+ ordering"]
    CAL --> AV["Availability check<br/>+ shift ?"]
    AV --> RESP[Select responsible]
    RESP --> REM((Reminder)):::core

    classDef core fill:#e8590c,stroke:#e8590c,color:#fff

```


