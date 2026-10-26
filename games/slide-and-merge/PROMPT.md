# Prompt: Slide & Merge

Paste the prompt below into Claude (or another capable coding model) to recreate this game as a single HTML file. Adjust anything you like before sending.

---

Build a complete, polished browser game called **Slide & Merge**, inspired by 2048, as **one self-contained HTML file** (inline CSS and JavaScript, no frameworks or build step; Google Fonts is the only allowed external resource, always with a system-font fallback). Use original characters and artwork drawn in code. Do not copy any trademarked characters, names or logos.

## The game

Slide every tile at once; matching tiles merge into their sum. Reach the goal tile before the board fills.

Menu text to show the player:

> Swipe to slide every tile at once. Two matching tiles merge into their sum. Reach the goal tile before the board fills up.

## Controls (phone first)

Swipe to slide; Undo and Restart buttons. Arrow keys also work.

Touch must feel good on a phone held in portrait. Add matching keyboard controls for desktop.

## Start menu settings

Show a start card with segmented buttons for each setting, remembered between visits:

- **Board**: 4×4, 5×5, 6×6
- **Undos**: None, 3, Unlimited
- **Rock tiles**: Off, On

## Levels

7 levels that unlock in order, shown as a numbered grid with a lock icon on locked ones. The selected level's description appears under the grid:

1. Reach 128
2. Reach 256
3. Reach 512
4. Reach 1024
5. Reach 2048
6. Reach 4096
7. Reach 8192

## Challenges

A collapsible checklist on the start card. When the player completes one, mark it done, save it, and show a short toast:

- Reach any goal tile
- Make a 2048 tile
- Reach a goal in fewer moves than 0.6 × the goal
- Make 512 on 4×4 with rocks on
- Make 1024 on 6×6

## Look and feel

- Type: Righteous for display, system UI for body text
- Palette: background #1b1530, text #f5f0ff, accent #ffb547
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
