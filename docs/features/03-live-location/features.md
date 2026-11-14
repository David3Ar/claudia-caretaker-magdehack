# Feature 3 — Live Location + Emergency Alert · Features

> Part of [Feature 3](../03-live-location.md) · Next: [Flows](flows.md) · Mockup: [`mockup.html`](mockup.html)
> `C` = caregiver · `G` = senior · `A` = Claudia. Names (Grete, Jonas, Anna) and places are examples, as in [`design.html`](../../design.html).
> Requirement IDs follow [`specs/feature-spec.md`](../../specs/feature-spec.md) §2.3. IDs marked *proposed* are not in the spec yet.

## Why

**Pain point:** `C` cannot be with `G` all day. Not knowing whether `G` is safe is the constant background worry. Calling to check feels like control and costs both of them energy.

**Idea:** Claudia answers *"is she all right?"* before `C` has to ask, and turns *"something is wrong"* into one clear call to action.

## Features

| # | Feature | Who | What it does | Spec ID | Prio |
|---|---|---|---|---|---|
| 0 | **Hands-free** | G | Wake word **"Hey Claudia"** starts every conversation. After that `G` only talks: no tap to start, answer or end | HF-1 *proposed* (extends NFR-2) | M |
| 1 | **C sees G** | C | `G`'s location as a plain place name ("At home"), a map, and today's places in order | LOC-1 | M |
| 2 | **G sees C** | G | "Where is my son?" → coarse answer ("Jonas is at work"), never an address | LOC-2 | M, consent **open** |
| 3 | **Call request** | G → C | "Ask him to call me" → push to `C`; Claudia announces his call back, `G` answers by saying "yes" | LOC-3 | M |
| 4 | **Call Jonas (direct)** | G → C | "Hey Claudia, call Jonas" rings him at once, no question back; same as the *Call Jonas* button | LOC-4 *proposed* (part of MSG-1) | M |
| 5 | **Emergency alert** | G → all C | "Hey Claudia, help!", the Emergency button, or no answer → full-screen alert on `C` with `G`'s location | EMG-1, EMG-2, EMG-5 *proposed* | M |

### Explanation

- **Hands-free.** `G` says "Hey Claudia" from anywhere in the room. From then on she only talks. The phone can stay on the table. Buttons are a fallback, never a step.
- **C sees G.** Place name first ("At home since 11:20"), map second, today's places below. Normal movement never sends a push.
- **G sees C.** Coarse answer only ("at work"). Each `C` decides in the dashboard whether `G` may ask. If not: *"I can't see where Jonas is, but I can ask him to call you."*
- **Call request.** One notification with one button for `C`: *Call Grete*. When he calls back, Claudia announces it and `G` answers by voice; the call runs on speaker.
- **Call Jonas (direct).** For when `G` just wants to talk now. Claudia says *"Calling Jonas."* and rings. `C` sees *Grete is calling*.
- **Emergency alert.** "Hey Claudia, help!" works when `G` has fallen and can't reach the phone. No confirm step. Every `C` gets the full-screen coral alert with where she is.

## Hands-free rules (senior app)

| Rule | Why |
|---|---|
| Claudia always listens for "Hey Claudia"; a green dot on the home screen shows it | `G` may be across the room, or on the floor after a fall |
| Wake word alone opens voice mode (black screen); no touch needed | The phone can stay on the table |
| Claudia detects the end of speech; no stop button | Nothing to find or press |
| Every question Claudia asks is answered by voice; the screen shows the words to say ("Yes", "No, thanks") | Screen is a hint, never a step |
| Incoming calls are announced and accepted by voice, then run on speaker | No ringing phone to find |
| Call Jonas and Emergency buttons stay on the idle home screen as fallback only | Design principle: "Buttons for what can't wait" |

## Emergency triggers

| Trigger | Spec ID | Demo | Note |
|---|---|---|---|
| "Hey Claudia, help!" | EMG-5 *proposed* | **Yes** | Primary: works when `G` can't reach the phone |
| Emergency button | EMG-1 | **Yes** | Fallback, same place on every idle senior screen |
| Not responding | EMG-2 | **Yes** | Claudia's planned prompt (greeting, tablet check) gets no answer → escalate |
| Smart watch | EMG-3 | No | Smart watch = Could |
| What happens after | EMG-4 | example only | **open** |

## Who sees what

| Data | G | C (Jonas) | C (Anna) |
|---|---|---|---|
| G's location | — | Map + place + history | Map + place + history |
| C's location | Coarse place only, if `C` allows | — | — |
| Emergency alert | Spoken confirmation | Full-screen alert | Full-screen alert |
| Call request | Spoken confirmation | Notification | — (only the asked person) |
| Direct call | "Calling Jonas." | Incoming call | — |
