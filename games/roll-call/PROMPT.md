# Prompt: Roll Call

Paste the prompt below into Claude (or another capable coding model) to recreate this game as a single HTML file. Adjust anything you like before sending.

---

Build a complete, polished browser game called **Roll Call**, inspired by five-dice scorecard games, as **one self-contained HTML file** (inline CSS and JavaScript, no frameworks or build step; Google Fonts is the only allowed external resource, always with a system-font fallback). Use original characters and artwork drawn in code. Do not copy any trademarked characters, names or logos.

## The game

Five dice, thirteen categories. Roll up to three times a turn, hold the dice you want, then score one row. Upper-section bonus at 63 and bonus fives.

Menu text to show the player:

> Five dice and thirteen rows. Roll up to three times a turn, hold the dice you like, then score one row. Each row only gets used once. Hit 63 in the top section for a 35-point bonus.

## Controls (phone first)

Tap Roll, tap dice to hold them, tap a scorecard row to score it. Possible scores preview in gold.

Touch must feel good on a phone held in portrait. Add matching keyboard controls for desktop.

## Start menu settings

Show a start card with segmented buttons for each setting, remembered between visits:

- **Players**: Solo, 2, 3, 4, Vs CPU
- **Show possible scores**: On, Off
- **Five of a kind counts as full house**: On, Off

## Challenges

A collapsible checklist on the start card. When the player completes one, mark it done, save it, and show a short toast:

- Roll five of a kind
- Score a large straight on the first roll
- Earn the upper-section bonus
- Score 250+ in a game
- Score 300+ in a game
- Beat the CPU

## Look and feel

- Type: Bowlby One for display, system UI for body text
- Palette: background #16301f, text #f3f7ef, accent #ffcc4d
- Layout: logical canvas 360×660, scaled to fit the screen
- A score/status strip at the top and a one-line control hint at the bottom. End-of-game and level-clear cards offer a clear next action (retry, next level, menu).
- Particles, small animations and screen feedback for hits, clears and wins. Keep motion purposeful.

## Technical requirements

- Render the playfield on a `<canvas>` at a fixed logical size, scaled to fit the available space with devicePixelRatio for sharpness. Clamp frame delta time (0 to 50 ms) so tab switches never break physics.
- Use pointer events for touch and mouse, with `touch-action: none` on the play area so the page never scrolls while playing.
- Respect safe-area insets (`env(safe-area-inset-*)`), keep at least a 16px side gutter, and never scroll horizontally at 360–400px widths.
- Save settings, unlocked levels, best scores and completed challenges in `localStorage`, wrapped in try/catch so the game still works when storage is blocked.
- No `alert()`/`confirm()`/`prompt()`; build any confirmation into the page.
- Test it: the game must load without console errors, start from the menu, and be playable start to finish.
