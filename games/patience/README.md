# Patience

**Klondike solitaire.**

▶ **Play:** [https://dougm1966.github.io/1off-1file-games/games/patience/](https://dougm1966.github.io/1off-1file-games/games/patience/) · or open [`index.html`](index.html) in any browser

| | |
|---|---|
| Type | Puzzle |
| Inspired by | Klondike solitaire |
| Built for | phones (portrait, touch); also works with mouse and keyboard |

## How it plays

Klondike solitaire with tap-to-move, drag-and-drop, undo, draw 1 or 3, and auto-finish.

> Klondike solitaire. Build the four suits up from Ace to King. In the columns, stack down in alternating colors. Only Kings go in empty columns.

## Controls

Tap a card to send it to its best spot, or drag it. Tap the stock to draw; Undo and New deal buttons.

## Settings

| Setting | Options |
|---|---|
| Draw | 1 card · 3 cards |
| Scoring | Standard · Vegas · None |
| Auto-finish | On · Off |
| Card backs | Blue · Red · Green |

## Challenges

A checklist in the menu that saves on your device:

- [ ] Win a game
- [ ] Win with draw 3
- [ ] Win in under 5 minutes
- [ ] Win without using undo
- [ ] Finish a Vegas game in the black
- [ ] Win 5 games

## Look and feel

- Type: Playfair Display for display, system UI for body text
- Palette: background #0f3b2c, text #f4f1e6, accent #f2c14e
- Layout: logical canvas 360×620, scaled to fit the screen

## Technical notes

- One self-contained HTML file: inline CSS and JavaScript, no build step, no libraries. The only external request is Google Fonts, with system-font fallbacks.
- Settings, unlocked levels, best scores and challenges are stored in the browser's `localStorage`, per device.
- Respects phone safe areas (notches) and never scrolls sideways.
- Recreate or remix it with [`PROMPT.md`](PROMPT.md).
