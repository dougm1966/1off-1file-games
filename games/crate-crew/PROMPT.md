# Prompt: Crate Crew

Paste the prompt below into Claude (or another capable coding model) to recreate this game as a single HTML file. Adjust anything you like before sending.

---

Build a complete, polished browser game called **Crate Crew**, inspired by Sokoban, as **one self-contained HTML file** (inline CSS and JavaScript, no frameworks or build step; Google Fonts is the only allowed external resource, always with a system-font fallback). Use original characters and artwork drawn in code. Do not copy any trademarked characters, names or logos.

## The game

Push every crate onto a dock. You can only push, never pull, one crate at a time. Fifteen levels, all guaranteed solvable; levels 1–9 show the shortest possible solution.

Menu text to show the player:

> Push every crate onto a dock. You can only push, never pull, and only one crate at a time. Plan ahead so nothing gets stuck in a corner.

## Controls (phone first)

Swipe or use the on-screen pad to walk; Undo and Restart buttons. Arrow keys and Z also work.

Touch must feel good on a phone held in portrait. Add matching keyboard controls for desktop.

## Start menu settings

Show a start card with segmented buttons for each setting, remembered between visits:

- **Controls**: Swipe + pad, Swipe only, Pad only
- **Undo**: On, Off
- **Look**: Warehouse, Lab

## Levels

15 levels that unlock in order, shown as a numbered grid with a lock icon on locked ones. The selected level's description appears under the grid:

1. Level 1 · 2 crates · best 8 moves
2. Level 2 · 2 crates · best 14 moves
3. Level 3 · 2 crates · best 25 moves
4. Level 4 · 3 crates · best 24 moves
5. Level 5 · 3 crates · best 29 moves
6. Level 6 · 3 crates · best 35 moves
7. Level 7 · 3 crates · best 41 moves
8. Level 8 · 3 crates · best 49 moves
9. Level 9 · 4 crates · best 50 moves
10. Level 10 · 4 crates
11. Level 11 · 4 crates
12. Level 12 · 4 crates
13. Level 13 · 5 crates
14. Level 14 · 5 crates
15. Level 15 · 5 crates

## Challenges

A collapsible checklist on the start card. When the player completes one, mark it done, save it, and show a short toast:

- Solve a level in the shortest possible moves
- Solve a level without undo
- Clear level 5
- Clear level 10
- Clear all 15 levels

## Look and feel

- Type: Russo One for display, system UI for body text
- Palette: background #1d1a16, text #f4ede1, accent #f2a93b
- Layout: logical canvas 360×560, scaled to fit the screen
- A score/status strip at the top and a one-line control hint at the bottom. End-of-game and level-clear cards offer a clear next action (retry, next level, menu).
- Particles, small animations and screen feedback for hits, clears and wins. Keep motion purposeful.

## Technical requirements

- Render the playfield on a `<canvas>` at a fixed logical size, scaled to fit the available space with devicePixelRatio for sharpness. Clamp frame delta time (0 to 50 ms) so tab switches never break physics.
- Use pointer events for touch and mouse, with `touch-action: none` on the play area so the page never scrolls while playing.
- Respect safe-area insets (`env(safe-area-inset-*)`), keep at least a 16px side gutter, and never scroll horizontally at 360–400px widths.
- Save settings, unlocked levels, best scores and completed challenges in `localStorage`, wrapped in try/catch so the game still works when storage is blocked.
- No `alert()`/`confirm()`/`prompt()`; build any confirmation into the page.
- Test it: the game must load without console errors, start from the menu, and be playable start to finish.
