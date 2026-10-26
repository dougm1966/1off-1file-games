# Stack Shift

**Falling-blocks stacker.**

▶ **Play:** [https://dougm1966.github.io/1off-1file-games/games/stack-shift/](https://dougm1966.github.io/1off-1file-games/games/stack-shift/) · or open [`index.html`](index.html) in any browser

| | |
|---|---|
| Type | Puzzle |
| Inspired by | Tetris-style falling blocks |
| Built for | phones (portrait, touch); also works with mouse and keyboard |

## How it plays

Classic falling-block stacking with seven-piece bag randomizer, ghost piece, hold slot and a three-piece next queue. Clear lines to score and level up.

## Controls

On the board: drag sideways to move, tap to rotate, swipe down fast to hard-drop, drag down slowly to soft-drop. A button row offers left, right, rotate, soft drop, hard drop and hold.

## Rules and features

- Speed increases every 10 lines; 1/2/3/4-line clears score 100/300/500/800 × level.
- Pause button and saved best score.

## Look and feel

- Type: Bungee + Space Mono
- Palette: navy (#121a33) with yellow accent (#ffcf3f); bevelled blocks in the classic seven colors
- Layout: board canvas plus side rail for hold/next/score

## Technical notes

- One self-contained HTML file: inline CSS and JavaScript, no build step, no libraries. The only external request is Google Fonts, with system-font fallbacks.
- Settings, unlocked levels, best scores and challenges are stored in the browser's `localStorage`, per device.
- Respects phone safe areas (notches) and never scrolls sideways.
- Recreate or remix it with [`PROMPT.md`](PROMPT.md).
