# Specs

> One folder per core feature: `spec.md` and flow HTML in the folder root, images in `img/`. Basis for the pitch deck. Nothing here is invented beyond the sources; undecided items are marked **open**.

**Roles:** `G` = senior · `C` = family caregiver · `A` = Claudia, the voice agent
**Priority:** `M` Must · `S` Should · `C` Could · **open** = not decided yet

| # | Core feature | Spec | Pitch material |
|---|---|---|---|
| 1 | Calendar / Scheduling | [`01-calendar/spec.md`](01-calendar/spec.md) | Six flows, step by step in [`01-calendar/flows.html`](01-calendar/flows.html); PNGs of flow 1 in [`01-calendar/img/`](01-calendar/img/) |
| 2 | Pill Checker | [`02-pill-checker/spec.md`](02-pill-checker/spec.md) | Six flows, step by step in [`02-pill-checker/flows.html`](02-pill-checker/flows.html); PNGs of all flows in [`02-pill-checker/img/`](02-pill-checker/img/) |
| 3 | Live Location + Emergency Alert | [`03-live-location/spec.md`](03-live-location/spec.md) | Five flows, step by step in [`03-live-location/flows.html`](03-live-location/flows.html); PNGs of all flows in [`03-live-location/img/`](03-live-location/img/) |
| 4 | QA / Setup | [`04-qa-setup/spec.md`](04-qa-setup/spec.md) | — |

## Product

| | |
|---|---|
| Problem | Family caregivers carry long-term stress and constant worry; the senior lives alone and the caregiver is the only lifeline |
| Solution | Voice-first agent that helps `G` through the day and gives `C` visibility and relief |
| Demo scope | 4 core features (all `M`): Calendar, Pill Checker, Live Location + Emergency, QA / Setup |
| Surfaces | Senior app (voice + large buttons) · caregiver app · web dashboard |
| Business model | Monthly subscription · add-ons (automatic pill purchase, delivery fees) · delivery partnerships |

## Shared functional requirements

| ID | Requirement | Prio | Status |
|---|---|---|---|
| X-1 | Web app + UI | M | defined |
| X-2 | Multilingual | M | languages **open** |
| X-3 | Caregiver dashboard: steer the agent, see status confirmations | M | defined |
| X-4 | Reminders with confirmation | M | defined |
| X-5 | Theme: caregiver app and web dashboard are dark by default, the senior app is light by default; each user can switch in settings | M | defined |

## Shared non-functional requirements

| ID | Area | Requirement | Source | Status |
|---|---|---|---|---|
| NFR-1 | Simplicity | Usable by non-technical people; technical concepts are abstracted into everyday words | design brief | defined |
| NFR-2 | Voice first | Every function reachable by voice; buttons only for core information and core actions such as emergency | design brief | defined |
| NFR-3 | Legibility | Senior app: large type (nothing to read below 22px), high contrast, large buttons in fixed positions | `design.html` | defined |
| NFR-4 | Platform | Cross-platform app on any phone; web dashboard for `C`; Siri integration | `project.md` | Siri scope **open** |
| NFR-5 | Language | Multilingual | story map | languages **open** |
| NFR-6 | Voice response time | Conversation feels live | — | target **open** |
| NFR-7 | Cost | Voice agent and cloud storage costs are covered by the subscription | `project.md` | price **open** |
| NFR-8 | Demo | Mockups and lightweight PoCs; voice via ElevenLabs; no tests | `AGENTS.md` | defined |

## After the demo

| Prio | Features |
|---|---|
| S | Daily check · message to anyone · delivery |
| C | Time capsule + questioning · ringtones · smart watch · custom voice (**open**: `C` or `S`) · camera identifies objects · smart home · pill box with sensors |

## Open points across features

- [ ] Languages for the demo
- [ ] Subscription price
- [ ] Direct mental-health feature for `C` (check-in, stress score, helpline) — listed as open in `project.md`
