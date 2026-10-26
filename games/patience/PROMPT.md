# Prompt: Patience

Paste the prompt below into Claude (or another capable coding model) to recreate this game as a single HTML file. Adjust anything you like before sending.

---

Build a complete, polished browser game called **Patience**, inspired by Klondike solitaire, as **one self-contained HTML file** (inline CSS and JavaScript, no frameworks or build step; Google Fonts is the only allowed external resource, always with a system-font fallback). Use original characters and artwork drawn in code. Do not copy any trademarked characters, names or logos.

## The game

Klondike solitaire with tap-to-move, drag-and-drop, undo, draw 1 or 3, and auto-finish.

Menu text to show the player:

> Klondike solitaire. Build the four suits up from Ace to King. In the columns, stack down in alternating colors. Only Kings go in empty columns.

## Controls (phone first)

Tap a card to send it to its best spot, or drag it. Tap the stock to draw; Undo and New deal buttons.

Touch must feel good on a phone held in portrait. Add matching keyboard controls for desktop.

## Start menu settings

Show a start card with segmented buttons for each setting, remembered between visits:

- **Draw**: 1 card, 3 cards
- **Scoring**: Standard, Vegas, None
- **Auto-finish**: On, Off
- **Card backs**: Blue, Red, Green

## Challenges

A collapsible checklist on the start card. When the player completes one, mark it done, save it, and show a short toast:

- Win a game
- Win with draw 3
- Win in under 5 minutes
- Win without using undo
- Finish a Vegas game in the black
- Win 5 games

## Look and feel

- Type: Playfair Display for display, system UI for body text
- Palette: background #0f3b2c, text #f4f1e6, accent #f2c14e
- Layout: logical canvas 360×620, scaled to fit the screen
- A score/status strip at the top and a one-line control hint at the bottom. End-of-game and level-clear cards offer a clear next action (retry, next level, menu).
- Particles, small animations and screen feedback for hits, clears and wins. Keep motion purposeful.

## Technical requirements

- Render the playfield on a `<canvas>` at a fixed logical size, scaled to fit the available space with devicePixelRatio for sharpness. Clamp frame delta time (0 to 50 ms) so tab switches never break physics.
- Use pointer events for touch and mouse, with `touch-action: none` on the play area so the page never scrolls while playing.
- Respect safe-area insets (`env(safe-area-inset-*)`), keep at least a 16px side gutter, and never scroll horizontally at 360–400px widths.
- Save settings, unlocked levels, best scores and completed challenges in `localStorage`, wrapped in try/catch so the game still works when storage is blocked.
- No `alert()`/`confirm()`/`prompt()`; build any confirmation into the page.
- Test it: the game must load without console errors, start from the menu, and be playable start to finish.
