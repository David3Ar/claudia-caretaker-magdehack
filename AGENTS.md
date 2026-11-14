# AGENTS.md

## Context

- Magdehack — hackathon for young founders.
- Goal: mockups, lightweight PoCs, a strong pitch.
- Priority: creativity, design, pain point → solution. Working code is secondary.
- **No tests.**

## Business

**Idea:** voice-first agent for seniors (`G`) that supports daily routines and gives family caregivers (`C`) visibility and relief.
Board title: *"To help regulate mental health of old people (Voice Agent)"*. Challenge: Pilot #6 — mental health of family caregivers.

**Problem:** caregivers face long-term stress, isolation, no low-barrier support; senior often lives alone, caregiver is only lifeline.

**Core demo features (all Must):**

| # | Feature | Spec |
|---|---|---|
| 1 | Calendar / Scheduling — shared events, availability check, assign responsible | `docs/features/01-calendar.md` |
| 2 | Pill Checker — plan from photo, scheduled check, escalation to C | `docs/features/02-pill-checker.md` |
| 3 | Live Location + Emergency Alert | `docs/features/03-live-location.md` |
| 4 | QA / Setup — talk to agent → diary, calendar, web, config | `docs/features/04-qa-setup.md` |

**Business model:** monthly subscription; add-ons (automatic pill purchase, delivery fees); delivery partnerships.

## Repo map

| Path | Content |
|---|---|
| [`AGENTS.md`](AGENTS.md) | Agent instructions (this file) |
| [`.claude/skills/`](.claude/skills/) | Project skills: `better-diagrams`, `ponytail`, `impeccable`, `ui-ux-pro-max` |
| [`docs/project.md`](docs/project.md) | Pitch brief |
| [`docs/user-story-map.md`](docs/user-story-map.md) | User story map + MoSCoW |
| [`docs/features/01-calendar.md`](docs/features/01-calendar.md) | Feature 1 — Calendar / Scheduling |
| [`docs/features/02-pill-checker.md`](docs/features/02-pill-checker.md) | Feature 2 — Pill Checker |
| [`docs/features/03-live-location.md`](docs/features/03-live-location.md) | Feature 3 — Live Location + Emergency Alert |
| [`docs/features/04-qa-setup.md`](docs/features/04-qa-setup.md) | Feature 4 — QA / Setup |

## Technical

- Public GitHub repo.
- Push directly to `main` (explicitly allowed).
- Small, atomic commits with descriptive messages. **No co-author trailer.**
- Voice agent demos: ElevenLabs.
- Pitch video: ElevenLabs video models.
- Phase 1 interactive mockups: Claude design mode in the browser.

## Writing docs

- Sharp, technical English. Bullets and tables over prose.
- Mermaid diagrams over text walls.
- Never invent facts; mark uncertain items as **open / to be discussed**.
