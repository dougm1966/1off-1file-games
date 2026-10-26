# Sort It Out

**Speed-sort tubes, organisms and blood cells.**

▶ **Play:** [https://dougm1966.github.io/1off-1file-games/games/sort-it-out/](https://dougm1966.github.io/1off-1file-games/games/sort-it-out/) · or open [`index.html`](index.html) in any browser

| | |
|---|---|
| Type | Lab |
| Inspired by | speed sorting |
| Built for | phones (portrait, touch); also works with mouse and keyboard |

## How it plays

Lab items fall toward four bins: drag each into the right one before it lands. Three benches: tests into tube colors, organisms into Gram reaction and shape, blood-cell images into cell type.

> Drag each item into its bin before it hits the bottom. Streaks score extra. Tube assignments follow common practice, but labs vary.

## Controls

Drag an item into a bin.

## Settings

| Setting | Options |
|---|---|
| Bench | Tube colors · Gram & shape · Blood cells |
| Mistakes allowed | 3 · 5 · Practice |
| Show the answer on a miss | On · Off |

## Levels

1. Steady
2. A bit faster
3. Brisk
4. Quick
5. Two at once
6. Rapid
7. Hectic
8. Rush
9. Frantic
10. Stat!

Levels unlock as you clear them.

## Challenges

A checklist in the menu that saves on your device:

- [ ] Clear a Tube colors level
- [ ] Clear a Gram & shape level
- [ ] Clear a Blood cells level
- [ ] Clear a level with zero misses
- [ ] Sort 15 in a row
- [ ] Clear level 10 (Stat!)

## Look and feel

- Type: IBM Plex Sans Condensed for display, system UI for body text
- Palette: background #0f1720, text #eef4f8, accent #7cc7e8
- Layout: logical canvas 360×600, scaled to fit the screen

## Technical notes

- One self-contained HTML file: inline CSS and JavaScript, no build step, no libraries. The only external request is Google Fonts, with system-font fallbacks.
- Settings, unlocked levels, best scores and challenges are stored in the browser's `localStorage`, per device.
- Respects phone safe areas (notches) and never scrolls sideways.
- Recreate or remix it with [`PROMPT.md`](PROMPT.md).
