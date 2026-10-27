# Sunset Run

[![Sunset Run](cover.webp)](https://dougm1966.github.io/1off-1file-games/games/sunset-run/)

**Pseudo-3D desert driving.**

▶ **Play:** [https://dougm1966.github.io/1off-1file-games/games/sunset-run/](https://dougm1966.github.io/1off-1file-games/games/sunset-run/) · or open [`index.html`](index.html) in any browser

| | |
|---|---|
| Type | Arcade |
| Inspired by | Out Run |
| Built for | phones (portrait, touch); also works with mouse and keyboard |

## How it plays

A pseudo-3D desert drive at sunset: weave through traffic and reach each checkpoint before the clock runs out, over 10 stages or in endless mode.

> Race the clock through the desert at sunset. Drag a finger sideways anywhere on the road to steer; the car follows your finger and the gas is automatic. Hold BRAKE to slow down. Pass each checkpoint to add time, and weave around traffic.

## Controls

Drag sideways anywhere on the board and the car follows smoothly; gas is automatic and a BRAKE button sits on the right. A setting gives ◀ ▶ GAS BRAKE buttons instead.

## Rules and features

- 10 stages that unlock, and 8 challenges.
- A header mute button and pause button; the game pauses itself when you switch apps.

## Settings

| Setting | Options |
|---|---|
| Steering | Drag on road · ◀ ▶ buttons |
| Drag sensitivity | Low · Medium · High |
| Top speed | Relaxed · Normal · Fast |
| Traffic | Light · Normal · Heavy |
| Clock | Relaxed · Normal · Tight |
| Mode | Stages · Endless |
| Controls side | Buttons right · Buttons left |
| Sound | On · Off |
| Vibration | On · Off |

## Levels

1. Dune Dawn
2. Cactus Alley
3. Mesa Road
4. Salt Flats
5. Canyon Run
6. Rattler Pass
7. Dust Devil
8. Red Rock Rise
9. Mirage Mile
10. Sunset Summit

Levels unlock as you clear them.

## Challenges

A checklist in the menu that saves on your device:

- [ ] Finish Mesa Road (stage 3)
- [ ] Finish Rattler Pass (stage 6)
- [ ] Finish Sunset Summit (stage 10)
- [ ] Pass 25 cars in one run
- [ ] Finish a stage without a crash
- [ ] Reach a checkpoint with 10+ seconds spare
- [ ] Drive 3 miles in Endless mode
- [ ] Hit top speed

## Look and feel

- Type: Russo One + Chakra Petch
- Palette: synthwave sunset: purple-to-orange sky, striped sun, desert sand, red-and-white rumble strips, orange accent (#ffb238)
- Layout: full-screen canvas, horizon 30% down

## Technical notes

- One self-contained HTML file: inline CSS and JavaScript, no build step, no libraries. The only external request is Google Fonts, with system-font fallbacks.
- Settings, unlocked levels, best scores and challenges are stored in the browser's `localStorage`, per device.
- Respects phone safe areas (notches) and never scrolls sideways.
- Recreate or remix it with [`PROMPT.md`](PROMPT.md).
