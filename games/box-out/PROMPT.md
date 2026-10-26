# Prompt: Box Out

Paste the prompt below into Claude (or another capable coding model) to recreate this game as a single HTML file. Adjust anything you like before sending.

---

Build a complete, polished browser game called **Box Out**, inspired by Dots and Boxes, as **one self-contained HTML file** (inline CSS and JavaScript, no frameworks or build step; Google Fonts is the only allowed external resource, always with a system-font fallback). Use original characters and artwork drawn in code. Do not copy any trademarked characters, names or logos.

## The game

Take turns drawing lines between dots on notebook paper. Close the fourth side of a box to claim it and go again. The hard CPU plays the chain game.

Menu text to show the player:

> Take turns drawing lines between dots. Draw the fourth side of a box to claim it, then go again. Most boxes wins. Watch out for handing over long chains.

## Controls (phone first)

Tap between two dots to draw a line.

Touch must feel good on a phone held in portrait. Add matching keyboard controls for desktop.

## Start menu settings

Show a start card with segmented buttons for each setting, remembered between visits:

- **Opponent**: Pass & play, CPU easy, CPU medium, CPU hard
- **Board**: 4×4, 5×6, 6×7
- **Goes first**: You / Blue, CPU / Red
- **Highlight 3-sided boxes**: On, Off
- **CPU speed**: Normal, Fast

## Challenges

A collapsible checklist on the start card. When the player completes one, mark it done, save it, and show a short toast:

- Beat the CPU
- Beat the hard CPU
- Close two boxes with one line
- Take 4+ boxes in one turn
- Beat the CPU without it scoring a box
- Win on the 6×7 board
- Finish a two-player game

## Look and feel

- Type: Patrick Hand for display, system UI for body text
- Palette: background #f6f1e3, text #24303d, accent #2f6fd6
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
