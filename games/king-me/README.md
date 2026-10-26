# King Me

**Checkers, friend or CPU.**

▶ **Play:** [https://dougm1966.github.io/1off-1file-games/games/king-me/](https://dougm1966.github.io/1off-1file-games/games/king-me/) · or open [`index.html`](index.html) in any browser

| | |
|---|---|
| Type | Two players |
| Inspired by | checkers |
| Built for | phones (portrait, touch); also works with mouse and keyboard |

## How it plays

Checkers with forced or optional captures, multi-jumps and kings, against a friend or the CPU.

> American checkers. Move diagonally forward and jump to capture. Reach the far row to become a king that moves both ways. Chain jumps happen in one move.

## Controls

Tap a piece, then tap a highlighted square to move. Legal moves are highlighted.

## Settings

| Setting | Options |
|---|---|
| Opponent | Pass & play · CPU easy · CPU medium · CPU hard |
| Forced captures | On (official) · Off |

## Challenges

A checklist in the menu that saves on your device:

- [ ] Beat the CPU
- [ ] Beat the hard CPU
- [ ] Crown a king
- [ ] Capture 3 in one move
- [ ] Beat the CPU without losing a piece
- [ ] Beat the CPU in 60 moves or fewer
- [ ] Finish a two-player game

## Look and feel

- Type: Abril Fatface for display, system UI for body text
- Palette: background #1e1410, text #f7ecdc, accent #e85d4a
- Layout: logical canvas 360×480, scaled to fit the screen

## Technical notes

- One self-contained HTML file: inline CSS and JavaScript, no build step, no libraries. The only external request is Google Fonts, with system-font fallbacks.
- Settings, unlocked levels, best scores and challenges are stored in the browser's `localStorage`, per device.
- Respects phone safe areas (notches) and never scrolls sideways.
- Recreate or remix it with [`PROMPT.md`](PROMPT.md).
