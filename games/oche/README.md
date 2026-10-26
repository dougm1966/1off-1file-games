# Oche

**Darts: x01, Cricket, Around the Clock.**

▶ **Play:** [https://dougm1966.github.io/1off-1file-games/games/oche/](https://dougm1966.github.io/1off-1file-games/games/oche/) · or open [`index.html`](index.html) in any browser

| | |
|---|---|
| Type | Two players |
| Inspired by | pub darts |
| Built for | phones (portrait, touch); also works with mouse and keyboard |

## How it plays

Darts with x01 (301/501, optional double-out), Cricket and Around the Clock. Your aim drifts like a real hand, so you time the release.

> Hold your finger on the board to aim. Your hand drifts, so watch the crosshair and let go at the right moment.

## Controls

Hold a finger on the board to aim (the crosshair appears above your finger and drifts), release to throw. Three darts per turn.

## Settings

| Setting | Options |
|---|---|
| Game | x01 · Cricket · Around the clock |
| Players | Solo · Two players · Vs CPU |
| x01 start | 301 · 501 |
| Double out | On · Off |
| Hand | Steady · Normal · Shaky |
| Around the clock: doubles/triples skip ahead | Off · On |

## Challenges

A checklist in the menu that saves on your device:

- [ ] Hit an inner bull
- [ ] Throw a 180
- [ ] Check out on a double
- [ ] Finish from 100 or more in one turn
- [ ] Win a game of Cricket
- [ ] Finish Around the Clock in 45 darts or fewer

## Look and feel

- Type: Alfa Slab One for display, system UI for body text
- Palette: background #14100c, text #f6efe2, accent #e2b04a
- Layout: logical canvas 360×620, scaled to fit the screen

## Technical notes

- One self-contained HTML file: inline CSS and JavaScript, no build step, no libraries. The only external request is Google Fonts, with system-font fallbacks.
- Settings, unlocked levels, best scores and challenges are stored in the browser's `localStorage`, per device.
- Respects phone safe areas (notches) and never scrolls sideways.
- Recreate or remix it with [`PROMPT.md`](PROMPT.md).
