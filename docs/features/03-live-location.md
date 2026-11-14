# Feature 3 — Live Location + Emergency Alert

> Source: whiteboard `IMG_2837`. Priority: **M** (Primary #6 + #9; core cluster incl. messaging).
> `C` = caregiver · `G` = senior. Requirements: [`specs/feature-spec.md`](../specs/feature-spec.md) §2.3 (LOC, EMG, MSG).

| Step | Document |
|---|---|
| 1. Features + explanation | [`03-live-location/features.md`](03-live-location/features.md) |
| 2. Flows (storyboards) | [`03-live-location/flows.md`](03-live-location/flows.md) |
| 3. Design mockup | [`03-live-location/mockup.html`](03-live-location/mockup.html) (open in a browser) |

## Scope

- **C sees G** — caregiver sees senior's location
- **G sees C** — in brackets on board → lower priority
  - "Where is my son?"
  - "Ask him to call me"
  - Direct "Call Jonas"
- **Emergency alert** — triggers: voice ("Hey Claudia, help!"), button, not responding, smart watch (Could)
- **Hands-free** — senior side is voice only after the wake word "Hey Claudia"

## Open points

- [ ] G sees C: in brackets on board → in demo or not?
- [ ] "Take action" after alert: who is called, in which order; call emergency services (112)? Shown as example only
- [ ] Not responding: retries, delays, which prompts count
- [ ] G cancels emergency by voice ("I'm all right"): allowed? within what time?
- [ ] Always-on wake word: battery, privacy, false triggers; ElevenLabs support for wake word in demo?
- [ ] Auto-answer calls on speaker vs. ask first
- [ ] Direct call not answered: offer call request automatically? voicemail?
- [ ] Notify C when G leaves home? (mockup: off by default, dashboard switch)
- [ ] Known places: who sets them (C in dashboard?)
- [ ] Location source: phone GPS only for demo?
- [ ] Privacy / consent for both directions; data retention of history
- [ ] Messaging part of this cluster: scope beyond call request and direct call undefined
- [ ] Smart watch trigger (Could) out of demo scope?
- [ ] Proposed IDs HF-1, LOC-4, EMG-5 to be added to `feature-spec.md`
