# Star Siege

**Space Invaders-style shooter.**

▶ **Play:** [https://dougm1966.github.io/1off-1file-games/games/star-siege/](https://dougm1966.github.io/1off-1file-games/games/star-siege/) · or open [`index.html`](index.html) in any browser

| | |
|---|---|
| Type | Arcade |
| Inspired by | Space Invaders |
| Built for | phones (portrait, touch); also works with mouse and keyboard |

## How it plays

Hold off a descending fleet of original alien designs from behind crumbling pixel shields; shoot the red saucer for a bonus.

> Hold the line against the descending fleet. Shields soak shots but crumble. Hit the red saucer for a bonus.
> Slide anywhere to move. Firing is automatic.

## Controls

Slide anywhere to move; firing is automatic.

## Rules and features

- The fleet speeds up as it thins out; waves start lower each time.
- Three lives; best score saved.

## Look and feel

- Type: Orbitron for display, system UI for body text
- Palette: background #070b18, text #e6f0ff, accent #5cf2c4
- Layout: logical canvas 360×600, scaled to fit the screen

## Technical notes

- One self-contained HTML file: inline CSS and JavaScript, no build step, no libraries. The only external request is Google Fonts, with system-font fallbacks.
- Settings, unlocked levels, best scores and challenges are stored in the browser's `localStorage`, per device.
- Respects phone safe areas (notches) and never scrolls sideways.
- Recreate or remix it with [`PROMPT.md`](PROMPT.md).
