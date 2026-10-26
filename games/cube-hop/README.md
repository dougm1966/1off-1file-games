# Cube Hop

[![Cube Hop](cover.webp)](https://dougm1966.github.io/1off-1file-games/games/cube-hop/)

**Pyramid cube-hopping.**

▶ **Play:** [https://dougm1966.github.io/1off-1file-games/games/cube-hop/](https://dougm1966.github.io/1off-1file-games/games/cube-hop/) · or open [`index.html`](index.html) in any browser

| | |
|---|---|
| Type | Arcade |
| Inspired by | Q*bert-style pyramid hopping (original characters) |
| Built for | phones (portrait, touch); also works with mouse and keyboard |

## How it plays

Hop on every cube of a pyramid to change its top color; later levels need two hits or toggle back. Dodge bouncing red balls and a green burr that hunts you, and don't hop off the edge.

> Hop on every cube until all the tops match the goal color shown up top. Dodge the red balls and the green burr that hunts you. Don't hop off the edge.
> Tap above-left, above-right, below-left or below-right of the hopper to jump that way.

## Controls

Tap diagonally around the hopper (above-left, above-right, below-left, below-right) to jump that way.

## Rules and features

- Three lives; level clear bonus.
- Best score saved.

## Look and feel

- Type: Baloo 2 for display, system UI for body text
- Palette: background #101433, text #f1f3ff, accent #ffcf33
- Layout: logical canvas 360×560, scaled to fit the screen

## Technical notes

- One self-contained HTML file: inline CSS and JavaScript, no build step, no libraries. The only external request is Google Fonts, with system-font fallbacks.
- Settings, unlocked levels, best scores and challenges are stored in the browser's `localStorage`, per device.
- Respects phone safe areas (notches) and never scrolls sideways.
- Recreate or remix it with [`PROMPT.md`](PROMPT.md).
