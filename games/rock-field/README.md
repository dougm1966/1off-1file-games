# Rock Field

[![Rock Field](cover.webp)](https://dougm1966.github.io/1off-1file-games/games/rock-field/)

**Asteroids-style vector shooter.**

▶ **Play:** [https://dougm1966.github.io/1off-1file-games/games/rock-field/](https://dougm1966.github.io/1off-1file-games/games/rock-field/) · or open [`index.html`](index.html) in any browser

| | |
|---|---|
| Type | Arcade |
| Inspired by | Asteroids |
| Built for | phones (portrait, touch); also works with mouse and keyboard |

## How it plays

Pilot a vector ship through 10 increasingly dangerous rock fields, splitting big rocks into small ones and dodging saucers.

> Blast the drifting rocks. Push the stick the way you want to fly: the ship turns to face it and thrusts harder the further you push. Hold FIRE to shoot. HYPER jumps to a random spot, with a risk.

## Controls

A thumb stick on the left: the ship turns to face the stick and thrusts harder the further you push. FIRE (hold to repeat) and HYPER buttons on the right; steering and firing work together. A 'Classic buttons' setting gives ⟲ ⟳ THRUST instead.

## Rules and features

- 10 levels that unlock, and 7 challenges.
- A header mute button and pause button; the game pauses itself when you switch apps.

## Settings

| Setting | Options |
|---|---|
| Controls | Stick + Fire · Classic buttons |
| Difficulty | Easy · Normal · Hard |
| Ships | 3 · 5 |
| Saucers | On · Off |
| Controls side | Buttons right · Buttons left |
| Sound | On · Off |
| Vibration | On · Off |

## Levels

1. Debris Drift
2. Gravel Run
3. Boulder Belt
4. Saucer Sighting
5. Crystal Cluster
6. Meteor Alley
7. Hot Rocks
8. Dust Storm
9. Iron Rain
10. The Last Field

Levels unlock as you clear them.

## Challenges

A checklist in the menu that saves on your device:

- [ ] Shatter 6 rocks within 10 seconds
- [ ] Shoot down a saucer
- [ ] Clear a level without losing a ship
- [ ] Survive 3 hyperspace jumps in one game
- [ ] Score 3000 in one game
- [ ] Clear Crystal Cluster (level 5)
- [ ] Clear The Last Field

## Look and feel

- Type: Audiowide for display, system UI for body text
- Palette: background #05060a, text #f2f4ff, accent #7df9ff
- Layout: logical canvas 360×640, scaled to fit the screen

## Technical notes

- One self-contained HTML file: inline CSS and JavaScript, no build step, no libraries. The only external request is Google Fonts, with system-font fallbacks.
- Settings, unlocked levels, best scores and challenges are stored in the browser's `localStorage`, per device.
- Respects phone safe areas (notches) and never scrolls sideways.
- Recreate or remix it with [`PROMPT.md`](PROMPT.md).
