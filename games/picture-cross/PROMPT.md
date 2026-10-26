# Prompt: Picture Cross

Paste the prompt below into Claude (or another capable coding model) to recreate this game as a single HTML file. Adjust anything you like before sending.

---

Build a complete, polished browser game called **Picture Cross**, inspired by nonograms / Picross, as **one self-contained HTML file** (inline CSS and JavaScript, no frameworks or build step; Google Fonts is the only allowed external resource, always with a system-font fallback). Use original characters and artwork drawn in code. Do not copy any trademarked characters, names or logos.

## The game

Fill the grid from the row and column clues to reveal a lab-themed picture, from 5×5 up to 15×15.

Menu text to show the player:

> The numbers give the runs of filled squares in each row and column, in order. Fill the grid to reveal the picture.

## Controls (phone first)

Tap or drag to fill; switch to ✕ to mark empty squares; Hint reveals a square.

Touch must feel good on a phone held in portrait. Add matching keyboard controls for desktop.

## Start menu settings

Show a start card with segmented buttons for each setting, remembered between visits:

- **Mistakes**: Checked · 3 strikes, Unchecked
- **Auto-mark finished lines**: On, Off
- **Hints per puzzle**: None, 1, 3

## Levels

15 levels that unlock in order, shown as a numbered grid with a lock icon on locked ones. The selected level's description appears under the grid:

1. 5×5 · Easy
2. 5×5 · Easy
3. 5×5 · Easy
4. 5×5 · Easy
5. 5×5 · Easy
6. 10×10 · Medium
7. 10×10 · Medium
8. 10×10 · Medium
9. 10×10 · Medium
10. 10×10 · Medium
11. 15×15 · Hard
12. 15×15 · Hard
13. 15×15 · Hard
14. 15×15 · Hard
15. 15×15 · Hard

## Challenges

A collapsible checklist on the start card. When the player completes one, mark it done, save it, and show a short toast:

- Finish all five 5×5 puzzles
- Solve a puzzle with zero mistakes (checked mode)
- Solve without hints
- Solve a 10×10 in under 2 minutes
- Solve a 15×15
- Solve all 15 puzzles

## Look and feel

- Type: DM Serif Display for display, system UI for body text
- Palette: background #f3efe6, text #2a2620, accent #2f6f8f
- Layout: logical canvas 360×540, scaled to fit the screen
- A score/status strip at the top and a one-line control hint at the bottom. End-of-game and level-clear cards offer a clear next action (retry, next level, menu).
- Particles, small animations and screen feedback for hits, clears and wins. Keep motion purposeful.

## Technical requirements

- Render the playfield on a `<canvas>` at a fixed logical size, scaled to fit the available space with devicePixelRatio for sharpness. Clamp frame delta time (0 to 50 ms) so tab switches never break physics.
- Use pointer events for touch and mouse, with `touch-action: none` on the play area so the page never scrolls while playing.
- Respect safe-area insets (`env(safe-area-inset-*)`), keep at least a 16px side gutter, and never scroll horizontally at 360–400px widths.
- Save settings, unlocked levels, best scores and completed challenges in `localStorage`, wrapped in try/catch so the game still works when storage is blocked.
- No `alert()`/`confirm()`/`prompt()`; build any confirmation into the page.
- Test it: the game must load without console errors, start from the menu, and be playable start to finish.
