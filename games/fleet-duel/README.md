# Fleet Duel

**Battleship, pass-and-play or CPU.**

▶ **Play:** [https://dougm1966.github.io/1off-1file-games/games/fleet-duel/](https://dougm1966.github.io/1off-1file-games/games/fleet-duel/) · or open [`index.html`](index.html) in any browser

| | |
|---|---|
| Type | Two players |
| Inspired by | Battleship |
| Built for | phones (portrait, touch); also works with mouse and keyboard |

## How it plays

Place your fleet, then take turns firing at the hidden enemy grid. Pass-and-play hides each board between turns; the CPU hunts and targets.

> Battleship. Hide your fleet, then take turns firing at the enemy grid. Sink every ship to win. In two-player mode, pass the phone between turns.

## Controls

Tap to place and rotate ships during setup, then tap enemy squares to fire.

## Settings

| Setting | Options |
|---|---|
| Opponent | CPU · CPU hard · Pass & play |
| Fleet | 5 ships · 4 ships · quicker |
| Salvo (one shot per ship afloat) | Off · On |
| After a hit | Turn passes · Shoot again |

## Challenges

A checklist in the menu that saves on your device:

- [ ] Beat the CPU
- [ ] Beat the hard CPU
- [ ] Win without losing a ship
- [ ] Win in 45 shots or fewer
- [ ] Hit 5 in a row
- [ ] Win a salvo game
- [ ] Finish a two-player battle

## Look and feel

- Type: Black Ops One for display, system UI for body text
- Palette: background #0a1a2a, text #e6f1fb, accent #ff6b4a
- Layout: logical canvas 360×620, scaled to fit the screen

## Technical notes

- One self-contained HTML file: inline CSS and JavaScript, no build step, no libraries. The only external request is Google Fonts, with system-font fallbacks.
- Settings, unlocked levels, best scores and challenges are stored in the browser's `localStorage`, per device.
- Respects phone safe areas (notches) and never scrolls sideways.
- Recreate or remix it with [`PROMPT.md`](PROMPT.md).
