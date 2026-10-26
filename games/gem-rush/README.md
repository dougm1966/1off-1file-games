# Gem Rush

**Match-3 gems with 15 levels.**

▶ **Play:** [https://dougm1966.github.io/1off-1file-games/games/gem-rush/](https://dougm1966.github.io/1off-1file-games/games/gem-rush/) · or open [`index.html`](index.html) in any browser

| | |
|---|---|
| Type | Puzzle |
| Inspired by | match-3 gem games |
| Built for | phones (portrait, touch); also works with mouse and keyboard |

## How it plays

Swap neighbouring gems to line up three or more. Four in a row makes a striped gem, an L or T makes a bomb, five makes a rainbow gem; levels have score or collect goals within a move limit.

> Swap neighboring gems to line up three or more. Match 4 for a striped gem that clears a line, an L or T for a bomb, and 5 for a rainbow gem that clears one whole color.

## Controls

Swipe a gem into a neighbour to swap.

## Settings

| Setting | Options |
|---|---|
| Gem colors | 5 · easier · 6 · 7 · harder |
| Moves | +6 · Standard · −4 |
| Hints when idle | On · Off |
| Animation | Fast · Normal · Slow |

## Levels

1. Score 2400
2. Score 3300
3. Collect 18 green
4. Score 5100
5. Score 6000
6. Collect 24 red
7. Score 7800
8. Score 8700
9. Collect 30 green
10. Score 10500
11. Score 11400
12. Collect 36 red
13. Score 13200
14. Score 14100
15. Collect 42 green

Levels unlock as you clear them.

## Challenges

A checklist in the menu that saves on your device:

- [ ] Make a bomb gem
- [ ] Make a rainbow gem
- [ ] Chain a 5× cascade
- [ ] Clear a level with 5+ moves left
- [ ] Clear all 15 levels

## Look and feel

- Type: Baloo 2 for display, system UI for body text
- Palette: background #170d2b, text #f7f0ff, accent #ff7ad9
- Layout: logical canvas 360×560, scaled to fit the screen

## Technical notes

- One self-contained HTML file: inline CSS and JavaScript, no build step, no libraries. The only external request is Google Fonts, with system-font fallbacks.
- Settings, unlocked levels, best scores and challenges are stored in the browser's `localStorage`, per device.
- Respects phone safe areas (notches) and never scrolls sideways.
- Recreate or remix it with [`PROMPT.md`](PROMPT.md).
