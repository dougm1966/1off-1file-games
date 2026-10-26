# Prompt: King Me

Paste the prompt below into Claude (or another capable coding model) to recreate this game as a single HTML file. Adjust anything you like before sending.

---

Build a complete, polished browser game called **King Me**, inspired by checkers, as **one self-contained HTML file** (inline CSS and JavaScript, no frameworks or build step; Google Fonts is the only allowed external resource, always with a system-font fallback). Use original characters and artwork drawn in code. Do not copy any trademarked characters, names or logos.

## The game

Checkers with forced or optional captures, multi-jumps and kings, against a friend or the CPU.

Menu text to show the player:

> American checkers. Move diagonally forward and jump to capture. Reach the far row to become a king that moves both ways. Chain jumps happen in one move.

## Controls (phone first)

Tap a piece, then tap a highlighted square to move. Legal moves are highlighted.

Touch must feel good on a phone held in portrait. Add matching keyboard controls for desktop.

## Start menu settings

Show a start card with segmented buttons for each setting, remembered between visits:

- **Opponent**: Pass & play, CPU easy, CPU medium, CPU hard
- **Forced captures**: On (official), Off

## Challenges

A collapsible checklist on the start card. When the player completes one, mark it done, save it, and show a short toast:

- Beat the CPU
- Beat the hard CPU
- Crown a king
- Capture 3 in one move
- Beat the CPU without losing a piece
- Beat the CPU in 60 moves or fewer
- Finish a two-player game

## Look and feel

- Type: Abril Fatface for display, system UI for body text
- Palette: background #1e1410, text #f7ecdc, accent #e85d4a
- Layout: logical canvas 360×480, scaled to fit the screen
- A score/status strip at the top and a one-line control hint at the bottom. End-of-game and level-clear cards offer a clear next action (retry, next level, menu).
- Particles, small animations and screen feedback for hits, clears and wins. Keep motion purposeful.

## Technical requirements

- Render the playfield on a `<canvas>` at a fixed logical size, scaled to fit the available space with devicePixelRatio for sharpness. Clamp frame delta time (0 to 50 ms) so tab switches never break physics.
- Use pointer events for touch and mouse, with `touch-action: none` on the play area so the page never scrolls while playing.
- Respect safe-area insets (`env(safe-area-inset-*)`), keep at least a 16px side gutter, and never scroll horizontally at 360–400px widths.
- Save settings, unlocked levels, best scores and completed challenges in `localStorage`, wrapped in try/catch so the game still works when storage is blocked.
- No `alert()`/`confirm()`/`prompt()`; build any confirmation into the page.
- Test it: the game must load without console errors, start from the menu, and be playable start to finish.
