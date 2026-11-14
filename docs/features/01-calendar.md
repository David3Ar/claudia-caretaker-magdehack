# Feature 1 — Calendar / Scheduling

> Source: `todo/IMG_2834`, `IMG_2835`. Priority: **M** (Primary #4, core ✔).
> `C` = caregiver · `G` = senior

## Scope

- Internal calendar
- Events creatable by **C and G**
- Sync with personal calendar (C's external calendar — provider **open**)
- Task scheduler
  - Ask → document (agent asks G, logs answer)
  - Stack reminders + ordering
- Availability check (+ shift?) → select responsible → reminder

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

## Flow — task needs a responsible caregiver

```mermaid
sequenceDiagram
    actor G as Senior
    participant A as Voice Agent
    participant Cal as Calendar
    actor C as Caregiver(s)
    G->>A: new appointment (voice)
    A->>Cal: create event
    A->>Cal: availability check of caregivers
    Cal-->>A: free slots
    A->>C: request: who takes it?
    C-->>A: accept → responsible
    A->>Cal: assign responsible
    Cal-->>C: reminder
    Cal-->>G: reminder (voice)
```

## Open points

- [ ] "+ shift?" — shift event if nobody available? **to be discussed**
- [ ] "Ask → document": what is asked, where stored (diary?)
- [ ] Ordering logic of stacked reminders
- [ ] Which external calendars to sync
