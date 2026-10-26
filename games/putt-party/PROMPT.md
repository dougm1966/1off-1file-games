# Prompt: Putt Party

Paste the prompt below into Claude (or another capable coding model) to recreate this game as a single HTML file. Adjust anything you like before sending.

---

Build a complete, polished browser game called **Putt Party**, inspired by mini golf, as **one self-contained HTML file** (inline CSS and JavaScript, no frameworks or build step; Google Fonts is the only allowed external resource, always with a system-font fallback). Use original characters and artwork drawn in code. Do not copy any trademarked characters, names or logos.

## The game

Eighteen holes of mini golf with windmills, sand, water, bumpers, slopes and moving obstacles, for one to four players on one phone.

Menu text to show the player:

> Eighteen holes of mini golf with windmills, sand, water and slopes. Up to four players take turns on one phone.

## Controls (phone first)

Drag back anywhere like a slingshot and release to putt; the arrow shows direction and power.

Touch must feel good on a phone held in portrait. Add matching keyboard controls for desktop.

## Start menu settings

Show a start card with segmented buttons for each setting, remembered between visits:

- **Players**: 1, 2, 3, 4
- **Max strokes per hole**: 6, 8, 10
- **Aim arrow**: On, Off

## Levels

3 levels that unlock in order, shown as a numbered grid with a lock icon on locked ones. The selected level's description appears under the grid:

1. Front nine
2. Back nine
3. All eighteen

## Challenges

A collapsible checklist on the start card. When the player completes one, mark it done, save it, and show a short toast:

- Make a hole in one
- Make a birdie
- Finish a round under par
- Finish a round without hitting water
- Play all 18
- Finish a multiplayer round

## Look and feel

- Type: Lilita One for display, system UI for body text
- Palette: background #123222, text #f2fbe9, accent #ffd34d
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
