# Prompt: Mine Field

Paste the prompt below into Claude (or another capable coding model) to recreate this game as a single HTML file. Adjust anything you like before sending.

---

Build a complete, polished browser game called **Mine Field**, inspired by Minesweeper, as **one self-contained HTML file** (inline CSS and JavaScript, no frameworks or build step; Google Fonts is the only allowed external resource, always with a system-font fallback). Use original characters and artwork drawn in code. Do not copy any trademarked characters, names or logos.

## The game

Clear every square that isn't a mine; numbers show how many mines touch each square.

Menu text to show the player:

> Clear every square that isn't a mine. Each number tells you how many mines touch that square.

## Controls (phone first)

Tap to dig, long-press (or Flag mode) to flag, tap a number to clear around it (chording).

Touch must feel good on a phone held in portrait. Add matching keyboard controls for desktop.

## Start menu settings

Show a start card with segmented buttons for each setting, remembered between visits:

- **Field**: Easy 9×9, Medium 12×16, Hard 16×24
- **First tap**: Opens an area, Safe square only
- **Question marks**: Off, On

## Challenges

A collapsible checklist on the start card. When the player completes one, mark it done, save it, and show a short toast:

- Clear an Easy field
- Clear Easy in under 60 seconds
- Clear a Medium field
- Clear a Hard field
- Win without placing a single flag
- Use 10 number-taps (chords) in one game

## Look and feel

- Type: Space Grotesk for display, system UI for body text
- Palette: background #16201a, text #eef5ea, accent #f2c14e
- Layout: logical canvas 360×580, scaled to fit the screen
- A score/status strip at the top and a one-line control hint at the bottom. End-of-game and level-clear cards offer a clear next action (retry, next level, menu).
- Particles, small animations and screen feedback for hits, clears and wins. Keep motion purposeful.

## Technical requirements

- Render the playfield on a `<canvas>` at a fixed logical size, scaled to fit the available space with devicePixelRatio for sharpness. Clamp frame delta time (0 to 50 ms) so tab switches never break physics.
- Use pointer events for touch and mouse, with `touch-action: none` on the play area so the page never scrolls while playing.
- Respect safe-area insets (`env(safe-area-inset-*)`), keep at least a 16px side gutter, and never scroll horizontally at 360–400px widths.
- Save settings, unlocked levels, best scores and completed challenges in `localStorage`, wrapped in try/catch so the game still works when storage is blocked.
- No `alert()`/`confirm()`/`prompt()`; build any confirmation into the page.
- Test it: the game must load without console errors, start from the menu, and be playable start to finish.
