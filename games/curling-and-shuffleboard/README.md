# Curl & Shuffle

[![Curl & Shuffle](cover.webp)](https://dougm1966.github.io/1off-1file-games/games/curling-and-shuffleboard/)

**Curling and table shuffleboard, friend or CPU.**

▶ **Play:** [https://dougm1966.github.io/1off-1file-games/games/curling-and-shuffleboard/](https://dougm1966.github.io/1off-1file-games/games/curling-and-shuffleboard/) · or open [`index.html`](index.html) in any browser

| | |
|---|---|
| Type | Two players |
| Inspired by | curling and table shuffleboard |
| Built for | phones (portrait, touch); also works with mouse and keyboard |

## How it plays

Two games in one, pass-and-play or against a CPU: curling with ends, hammer and proper scoring, and table shuffleboard with 1-2-3 zones, hangers and knock-offs.

> Two games, one phone. Curling: drag back from the hack zone and release (angle sets the line, length sets the weight), pick IN or OUT curl, then hold SWEEP while the stone slides. Shuffleboard: flick a puck up the table. Play a friend, passing the phone, or the CPU.

## Controls

Curling: pick IN or OUT curl, drag back from the hack and release to throw, and hold the big SWEEP button while the stone travels to carry it farther and straighter. Shuffleboard: flick the puck from the flick zone.

## Rules and features

- A pass card between turns in two-player games.
- A header mute button and pause button; the game pauses itself when you switch apps.

## Settings

| Setting | Options |
|---|---|
| Game | Curling · Shuffleboard |
| Mode | vs CPU · 2 players |
| Curling: ends | 2 · 4 · 6 |
| Curling: stones each | 4 (short) · 8 (full) |
| Shuffleboard: target score | 11 · 15 · 21 |
| Ice / table speed | Slow · Normal · Fast |
| CPU skill | Easy · Normal · Hard |
| Controls side | Buttons right · Buttons left |
| Sound | On · Off |
| Vibration | On · Off |

## Challenges

A checklist in the menu that saves on your device:

- [ ] Sweep a stone into the house
- [ ] Land a stone on the button
- [ ] Knock an opposing stone out of play
- [ ] Score 2 or more in one curling end
- [ ] Win a curling match against the CPU
- [ ] Land a hanger in shuffleboard
- [ ] Win a shuffleboard match against the CPU

## Look and feel

- Type: system UI
- Palette: 
- Layout: 

## Technical notes

- One self-contained HTML file: inline CSS and JavaScript, no build step, no libraries. The only external request is Google Fonts, with system-font fallbacks.
- Settings, unlocked levels, best scores and challenges are stored in the browser's `localStorage`, per device.
- Respects phone safe areas (notches) and never scrolls sideways.
- Recreate or remix it with [`PROMPT.md`](PROMPT.md).
