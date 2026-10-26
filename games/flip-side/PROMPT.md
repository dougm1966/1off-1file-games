# Prompt: Flip Side

Paste the prompt below into Claude (or another capable coding model) to recreate this game as a single HTML file. Adjust anything you like before sending.

---

Build a complete, polished browser game called **Flip Side**, inspired by Reversi / Othello, as **one self-contained HTML file** (inline CSS and JavaScript, no frameworks or build step; Google Fonts is the only allowed external resource, always with a system-font fallback). Use original characters and artwork drawn in code. Do not copy any trademarked characters, names or logos.

## The game

Place discs to outflank and flip your opponent's. Most discs when the board fills wins.

Menu text to show the player:

> Reversi. Place a disc so it traps a line of your opponent's discs between yours, and every trapped disc flips to your color. Most discs at the end wins. Corners can't be flipped.

## Controls (phone first)

Tap one of the dots that marks a legal move.

Touch must feel good on a phone held in portrait. Add matching keyboard controls for desktop.

## Start menu settings

Show a start card with segmented buttons for each setting, remembered between visits:

- **Opponent**: Pass & play, CPU easy, CPU medium, CPU hard
- **Show legal moves**: On, Off

## Challenges

A collapsible checklist on the start card. When the player completes one, mark it done, save it, and show a short toast:

- Beat the CPU
- Beat the hard CPU
- Take a corner
- Flip 6+ discs in one move
- Beat the CPU with 40+ discs
- Wipe the CPU off the board
- Finish a two-player game

## Look and feel

- Type: Unbounded for display, system UI for body text
- Palette: background #0f2a24, text #effaf5, accent #5ce0b0
- Layout: logical canvas 360×470, scaled to fit the screen
- A score/status strip at the top and a one-line control hint at the bottom. End-of-game and level-clear cards offer a clear next action (retry, next level, menu).
- Particles, small animations and screen feedback for hits, clears and wins. Keep motion purposeful.

## Technical requirements

- Render the playfield on a `<canvas>` at a fixed logical size, scaled to fit the available space with devicePixelRatio for sharpness. Clamp frame delta time (0 to 50 ms) so tab switches never break physics.
- Use pointer events for touch and mouse, with `touch-action: none` on the play area so the page never scrolls while playing.
- Respect safe-area insets (`env(safe-area-inset-*)`), keep at least a 16px side gutter, and never scroll horizontally at 360–400px widths.
- Save settings, unlocked levels, best scores and completed challenges in `localStorage`, wrapped in try/catch so the game still works when storage is blocked.
- No `alert()`/`confirm()`/`prompt()`; build any confirmation into the page.
- Test it: the game must load without console errors, start from the menu, and be playable start to finish.
