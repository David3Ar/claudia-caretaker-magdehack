# Pilot #6 — Mental Health of Family Caregivers

> Because ‘I did’ feels better than ‘I wish I had.’

## Problem

Pilot #6 focuses on family caregivers who face long-term emotional strain, stress and social isolation. Their own needs are easily overlooked, and support can be hard to fit into daily life. Even after arranging a ride or reminding a parent to take their tablets, a caregiver may spend the day wondering what happened and blaming themselves for missing a check-in.

| Driver | Impact on caregiver |
|---|---|
| Senior lives alone | Caregiver is the only lifeline |
| Care is time-intensive | No time for self |
| Help is hard to find | Load stays with family |
| No feedback on help quality | Constant worry |
| Fewer children in DE | More load per caregiver |

## Solution

Claudia helps seniors manage daily routines by voice and shares their confirmations with the family.

- **For seniors**, asking what's on today, confirming tablets or calling family takes a few spoken words. That independence supports quality of life at home.
- **For caregivers**, Claudia takes on repetitive reminders, follows up and automatically records the answers in the family diary. Over time, those entries build a shared care history. A relative can look up what Mum said after breakfast or who took her to her last appointment without asking her to tell the story again.
- **For the family**, a shared calendar shows who agreed to help. If plans change, another relative can take over the ride when they see the request. Fewer coordination calls leave more time to enjoy each other's company.


## System Map

```mermaid
flowchart LR
    S(["👵 Senior"]) <-->|voice| A["🤖 Voice Agent"]
    A <-->|status / control| C(["🧑 Caregiver"])

    A --- UX["<b>UX</b><br/>any phone<br/>voice + big buttons<br/>Siri"]
    A --- EN["<b>Engagement</b><br/>nostalgia board<br/>diary mode<br/>custom voice"]
    A --- HE["<b>Health</b><br/>calendar + reminders<br/>confirmation loop<br/>pill checker"]
    A --- CG["<b>Cognition</b><br/>proactive prompts<br/>save + compare answers<br/>trend detection"]

    C --- DB["<b>Dashboard</b><br/>steer agent<br/>push content<br/>outside mode + location"]
    HE -.->|confirmations| DB
    CG -.->|alerts| DB

    classDef actor fill:#1e3a5f,stroke:#1e3a5f,color:#fff
    classDef core fill:#e8590c,stroke:#e8590c,color:#fff
    classDef mod fill:#f1f3f5,stroke:#868e96,color:#212529
    class S,C actor
    class A core
    class UX,EN,HE,CG,DB mod
```

## Features

| Module | Features |
|---|---|
| **UX** | · Cross-platform app · voice-first · key actions as buttons · Siri integration · voice |
| **Senior** | Reminders · Location of caregivers · QA on interests e.g. TV Program |
| **Caregiver** | Dashboard · remote steering · status confirmations · outside mode + location · remote calendar · "Resposability tracking". |
| **Engagement** | remote family content · diary mode · quick call and call announcements |
| **Cognition** | Agent-initiated dialogues: nostalgie + response logging & change detection |
| **Health** | Calendar + reminders with confirmation · pill checker |





<br />


<br />

## Business Model

- monthly subscription mode (needed to cover voice agent and clouds storage costs)

- add-on subscriptions : Automtatic Pill purchase plan, Delivery Fee's
- Partnership with Deliverer Companies

## Open Points

- [ ] Direct caregiver mental-health feature (check-in, stress score, peer/helpline)
- [ ] Clarify "B40C" next to pill checker
- [ ] Confirm "Diary mode"
