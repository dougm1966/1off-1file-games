# Prompt: Fleet Duel

Paste the prompt below into Claude (or another capable coding model) to recreate this game as a single HTML file. Adjust anything you like before sending.

---

Build a complete, polished browser game called **Fleet Duel**, inspired by Battleship, as **one self-contained HTML file** (inline CSS and JavaScript, no frameworks or build step; Google Fonts is the only allowed external resource, always with a system-font fallback). Use original characters and artwork drawn in code. Do not copy any trademarked characters, names or logos.

## The game

Place your fleet, then take turns firing at the hidden enemy grid. Pass-and-play hides each board between turns; the CPU hunts and targets.

Menu text to show the player:

> Battleship. Hide your fleet, then take turns firing at the enemy grid. Sink every ship to win. In two-player mode, pass the phone between turns.

## Controls (phone first)

Tap to place and rotate ships during setup, then tap enemy squares to fire.

Touch must feel good on a phone held in portrait. Add matching keyboard controls for desktop.

## Start menu settings

Show a start card with segmented buttons for each setting, remembered between visits:

- **Opponent**: CPU, CPU hard, Pass & play
- **Fleet**: 5 ships, 4 ships · quicker
- **Salvo (one shot per ship afloat)**: Off, On
- **After a hit**: Turn passes, Shoot again

## Challenges

A collapsible checklist on the start card. When the player completes one, mark it done, save it, and show a short toast:

- Beat the CPU
- Beat the hard CPU
- Win without losing a ship
- Win in 45 shots or fewer
- Hit 5 in a row
- Win a salvo game
- Finish a two-player battle

## Look and feel

- Type: Black Ops One for display, system UI for body text
- Palette: background #0a1a2a, text #e6f1fb, accent #ff6b4a
- Layout: logical canvas 360×620, scaled to fit the screen
- A score/status strip at the top and a one-line control hint at the bottom. End-of-game and level-clear cards offer a clear next action (retry, next level, menu).
- Particles, small animations and screen feedback for hits, clears and wins. Keep motion purposeful.

## Technical requirements

- Render the playfield on a `<canvas>` at a fixed logical size, scaled to fit the available space with devicePixelRatio for sharpness. Clamp frame delta time (0 to 50 ms) so tab switches never break physics.
- Use pointer events for touch and mouse, with `touch-action: none` on the play area so the page never scrolls while playing.
- Respect safe-area insets (`env(safe-area-inset-*)`), keep at least a 16px side gutter, and never scroll horizontally at 360–400px widths.
- Save settings, unlocked levels, best scores and completed challenges in `localStorage`, wrapped in try/catch so the game still works when storage is blocked.
- No `alert()`/`confirm()`/`prompt()`; build any confirmation into the page.
- Test it: the game must load without console errors, start from the menu, and be playable start to finish.
