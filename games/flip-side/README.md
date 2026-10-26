# Flip Side

**Reversi / Othello, friend or CPU.**

▶ **Play:** [https://dougm1966.github.io/1off-1file-games/games/flip-side/](https://dougm1966.github.io/1off-1file-games/games/flip-side/) · or open [`index.html`](index.html) in any browser

| | |
|---|---|
| Type | Two players |
| Inspired by | Reversi / Othello |
| Built for | phones (portrait, touch); also works with mouse and keyboard |

## How it plays

Place discs to outflank and flip your opponent's. Most discs when the board fills wins.

> Reversi. Place a disc so it traps a line of your opponent's discs between yours, and every trapped disc flips to your color. Most discs at the end wins. Corners can't be flipped.

## Controls

Tap one of the dots that marks a legal move.

## Settings

| Setting | Options |
|---|---|
| Opponent | Pass & play · CPU easy · CPU medium · CPU hard |
| Show legal moves | On · Off |

## Challenges

A checklist in the menu that saves on your device:

- [ ] Beat the CPU
- [ ] Beat the hard CPU
- [ ] Take a corner
- [ ] Flip 6+ discs in one move
- [ ] Beat the CPU with 40+ discs
- [ ] Wipe the CPU off the board
- [ ] Finish a two-player game

## Look and feel

- Type: Unbounded for display, system UI for body text
- Palette: background #0f2a24, text #effaf5, accent #5ce0b0
- Layout: logical canvas 360×470, scaled to fit the screen

## Technical notes

- One self-contained HTML file: inline CSS and JavaScript, no build step, no libraries. The only external request is Google Fonts, with system-font fallbacks.
- Settings, unlocked levels, best scores and challenges are stored in the browser's `localStorage`, per device.
- Respects phone safe areas (notches) and never scrolls sideways.
- Recreate or remix it with [`PROMPT.md`](PROMPT.md).
