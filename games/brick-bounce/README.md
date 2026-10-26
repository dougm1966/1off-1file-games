# Brick Bounce

[![Brick Bounce](cover.webp)](https://dougm1966.github.io/1off-1file-games/games/brick-bounce/)

**Breakout-style brick breaker.**

▶ **Play:** [https://dougm1966.github.io/1off-1file-games/games/brick-bounce/](https://dougm1966.github.io/1off-1file-games/games/brick-bounce/) · or open [`index.html`](index.html) in any browser

| | |
|---|---|
| Type | Arcade |
| Inspired by | Breakout / Arkanoid |
| Built for | phones (portrait, touch); also works with mouse and keyboard |

## How it plays

Bounce a ball off your paddle to clear rows of bricks; five rotating layouts, two-hit bricks on later levels and a ball that speeds up.

> Clear every brick. Where the ball hits the paddle sets its angle.
> Slide anywhere to move the paddle, tap to launch.

## Controls

Slide anywhere to move the paddle (relative movement), tap to launch. Arrow keys and space also work.

## Rules and features

- Where the ball hits the paddle sets its angle.
- Three lives; best score saved.

## Look and feel

- Type: Righteous for display, system UI for body text
- Palette: background #14122b, text #f4f1ff, accent #ff8a3d
- Layout: logical canvas 360×620, scaled to fit the screen

## Technical notes

- One self-contained HTML file: inline CSS and JavaScript, no build step, no libraries. The only external request is Google Fonts, with system-font fallbacks.
- Settings, unlocked levels, best scores and challenges are stored in the browser's `localStorage`, per device.
- Respects phone safe areas (notches) and never scrolls sideways.
- Recreate or remix it with [`PROMPT.md`](PROMPT.md).
