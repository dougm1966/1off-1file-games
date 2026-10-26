# Prompt: Sort It Out

Paste the prompt below into Claude (or another capable coding model) to recreate this game as a single HTML file. Adjust anything you like before sending.

---

Build a complete, polished browser game called **Sort It Out**, inspired by speed sorting, as **one self-contained HTML file** (inline CSS and JavaScript, no frameworks or build step; Google Fonts is the only allowed external resource, always with a system-font fallback). Use original characters and artwork drawn in code. Do not copy any trademarked characters, names or logos.

## The game

Lab items fall toward four bins: drag each into the right one before it lands. Three benches: tests into tube colors, organisms into Gram reaction and shape, blood-cell images into cell type.

Menu text to show the player:

> Drag each item into its bin before it hits the bottom. Streaks score extra. Tube assignments follow common practice, but labs vary.

## Controls (phone first)

Drag an item into a bin.

Touch must feel good on a phone held in portrait. Add matching keyboard controls for desktop.

## Start menu settings

Show a start card with segmented buttons for each setting, remembered between visits:

- **Bench**: Tube colors, Gram & shape, Blood cells
- **Mistakes allowed**: 3, 5, Practice
- **Show the answer on a miss**: On, Off

## Levels

10 levels that unlock in order, shown as a numbered grid with a lock icon on locked ones. The selected level's description appears under the grid:

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

## Challenges

A collapsible checklist on the start card. When the player completes one, mark it done, save it, and show a short toast:

- Clear a Tube colors level
- Clear a Gram & shape level
- Clear a Blood cells level
- Clear a level with zero misses
- Sort 15 in a row
- Clear level 10 (Stat!)

## Look and feel

- Type: IBM Plex Sans Condensed for display, system UI for body text
- Palette: background #0f1720, text #eef4f8, accent #7cc7e8
- Layout: logical canvas 360×600, scaled to fit the screen
- A score/status strip at the top and a one-line control hint at the bottom. End-of-game and level-clear cards offer a clear next action (retry, next level, menu).
- Particles, small animations and screen feedback for hits, clears and wins. Keep motion purposeful.

## Technical requirements

- Render the playfield on a `<canvas>` at a fixed logical size, scaled to fit the available space with devicePixelRatio for sharpness. Clamp frame delta time (0 to 50 ms) so tab switches never break physics.
- Use pointer events for touch and mouse, with `touch-action: none` on the play area so the page never scrolls while playing.
- Respect safe-area insets (`env(safe-area-inset-*)`), keep at least a 16px side gutter, and never scroll horizontally at 360–400px widths.
- Save settings, unlocked levels, best scores and completed challenges in `localStorage`, wrapped in try/catch so the game still works when storage is blocked.
- No `alert()`/`confirm()`/`prompt()`; build any confirmation into the page.
- Test it: the game must load without console errors, start from the menu, and be playable start to finish.
