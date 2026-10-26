# Prompt: Drop Four

Paste the prompt below into Claude (or another capable coding model) to recreate this game as a single HTML file. Adjust anything you like before sending.

---

Build a complete, polished browser game called **Drop Four**, inspired by Connect Four, as **one self-contained HTML file** (inline CSS and JavaScript, no frameworks or build step; Google Fonts is the only allowed external resource, always with a system-font fallback). Use original characters and artwork drawn in code. Do not copy any trademarked characters, names or logos.

## The game

Drop discs into columns and line up four (or five on the big board) across, down or diagonally. CPU uses alpha-beta search.

Menu text to show the player:

> Take turns dropping pieces. First to line up four across, down or diagonally wins. The Connect 5 board needs five.

## Controls (phone first)

Tap a column to drop a disc. Number keys also work.

Touch must feel good on a phone held in portrait. Add matching keyboard controls for desktop.

## Start menu settings

Show a start card with segmented buttons for each setting, remembered between visits:

- **Opponent**: Pass & play, CPU easy, CPU medium, CPU hard
- **Board**: 7×6, 8×7, Connect 5 · 9×7
- **Goes first**: Red / You, Gold / CPU, Alternate
- **Move clock**: Off, 15s, 8s

## Challenges

A collapsible checklist on the start card. When the player completes one, mark it done, save it, and show a short toast:

- Beat the medium CPU
- Beat the hard CPU
- Beat the CPU 3 games in a row
- Beat the CPU in 8 moves or fewer
- Win with a diagonal
- Win a Connect 5 game

## Look and feel

- Type: Rubik for display, system UI for body text
- Palette: background #101a33, text #eef3ff, accent #ffcf3f
- Layout: logical canvas 360×520, scaled to fit the screen
- A score/status strip at the top and a one-line control hint at the bottom. End-of-game and level-clear cards offer a clear next action (retry, next level, menu).
- Particles, small animations and screen feedback for hits, clears and wins. Keep motion purposeful.

## Technical requirements

- Render the playfield on a `<canvas>` at a fixed logical size, scaled to fit the available space with devicePixelRatio for sharpness. Clamp frame delta time (0 to 50 ms) so tab switches never break physics.
- Use pointer events for touch and mouse, with `touch-action: none` on the play area so the page never scrolls while playing.
- Respect safe-area insets (`env(safe-area-inset-*)`), keep at least a 16px side gutter, and never scroll horizontally at 360–400px widths.
- Save settings, unlocked levels, best scores and completed challenges in `localStorage`, wrapped in try/catch so the game still works when storage is blocked.
- No `alert()`/`confirm()`/`prompt()`; build any confirmation into the page.
- Test it: the game must load without console errors, start from the menu, and be playable start to finish.
