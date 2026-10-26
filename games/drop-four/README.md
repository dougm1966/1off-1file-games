# Drop Four

**Connect Four, friend or CPU.**

▶ **Play:** [https://dougm1966.github.io/1off-1file-games/games/drop-four/](https://dougm1966.github.io/1off-1file-games/games/drop-four/) · or open [`index.html`](index.html) in any browser

| | |
|---|---|
| Type | Two players |
| Inspired by | Connect Four |
| Built for | phones (portrait, touch); also works with mouse and keyboard |

## How it plays

Drop discs into columns and line up four (or five on the big board) across, down or diagonally. CPU uses alpha-beta search.

> Take turns dropping pieces. First to line up four across, down or diagonally wins. The Connect 5 board needs five.

## Controls

Tap a column to drop a disc. Number keys also work.

## Settings

| Setting | Options |
|---|---|
| Opponent | Pass & play · CPU easy · CPU medium · CPU hard |
| Board | 7×6 · 8×7 · Connect 5 · 9×7 |
| Goes first | Red / You · Gold / CPU · Alternate |
| Move clock | Off · 15s · 8s |

## Challenges

A checklist in the menu that saves on your device:

- [ ] Beat the medium CPU
- [ ] Beat the hard CPU
- [ ] Beat the CPU 3 games in a row
- [ ] Beat the CPU in 8 moves or fewer
- [ ] Win with a diagonal
- [ ] Win a Connect 5 game

## Look and feel

- Type: Rubik for display, system UI for body text
- Palette: background #101a33, text #eef3ff, accent #ffcf3f
- Layout: logical canvas 360×520, scaled to fit the screen

## Technical notes

- One self-contained HTML file: inline CSS and JavaScript, no build step, no libraries. The only external request is Google Fonts, with system-font fallbacks.
- Settings, unlocked levels, best scores and challenges are stored in the browser's `localStorage`, per device.
- Respects phone safe areas (notches) and never scrolls sideways.
- Recreate or remix it with [`PROMPT.md`](PROMPT.md).
