# Coil

**Snake.**

▶ **Play:** [https://dougm1966.github.io/1off-1file-games/games/coil/](https://dougm1966.github.io/1off-1file-games/games/coil/) · or open [`index.html`](index.html) in any browser

| | |
|---|---|
| Type | Arcade |
| Inspired by | Snake |
| Built for | phones (portrait, touch); also works with mouse and keyboard |

## How it plays

Grow the snake by eating apples; golden stars are worth 50 but vanish fast. Speed rises as you grow.

> Eat apples to grow. Golden stars are worth 50 but vanish fast. Don't hit the walls or yourself.
> Swipe anywhere to turn.

## Controls

Swipe anywhere to turn; up to three turns can be queued. Arrow keys also work.

## Rules and features

- Hitting a wall or yourself ends the run.
- Best score saved.

## Look and feel

- Type: Silkscreen for display, system UI for body text
- Palette: background #0f1a12, text #e8f5e1, accent #b8f05a
- Layout: logical canvas 360×504, scaled to fit the screen

## Technical notes

- One self-contained HTML file: inline CSS and JavaScript, no build step, no libraries. The only external request is Google Fonts, with system-font fallbacks.
- Settings, unlocked levels, best scores and challenges are stored in the browser's `localStorage`, per device.
- Respects phone safe areas (notches) and never scrolls sideways.
- Recreate or remix it with [`PROMPT.md`](PROMPT.md).
