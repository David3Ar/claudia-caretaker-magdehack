# Pilotprojektsteckbrief #6 — Mental Health bei pflegenden Angehörigen

> Proactive voice agent for seniors → relief and transparency for family caregivers.

## Problem

**Core:** Family caregivers face long-term stress, emotional strain and isolation. They are overlooked, and no low-barrier support fits their daily routine.

| Driver | Impact on caregiver |
|---|---|
| Senior lives alone | Caregiver is the only lifeline |
| Care is time-intensive | No time for self |
| Help is hard to find | Load stays with family |
| No feedback on help quality | Constant worry |
| Fewer children in DE | More load per caregiver |

## Solution

A simple, voice-first agent app for every senior that **helps with daily routines** and **gives caregivers visibility**.


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

<br />

<br />

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
