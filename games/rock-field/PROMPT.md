# Prompt: Rock Field

Paste the prompt below into Claude (or another capable coding model) to recreate this game as a single HTML file. Adjust anything you like before sending.

---

Build a complete, polished browser game called **Rock Field**, inspired by Asteroids, as **one self-contained HTML file** (inline CSS and JavaScript, no frameworks or build step; Google Fonts is the only allowed external resource, always with a system-font fallback). Use original characters and artwork drawn in code. Do not copy any trademarked characters, names or logos.

## The game

Vector-style rock blasting: big rocks split into smaller, faster pieces.

Menu text to show the player:

> Blast the drifting rocks. Big ones split into smaller, faster pieces.
> Touch and hold where you want to go. The ship turns toward your finger, thrusts when it's far away, and fires when it's lined up.

## Controls (phone first)

Touch and hold: the ship turns toward your finger, thrusts when your finger is far away, and fires when lined up. Arrow keys plus space also work.

Touch must feel good on a phone held in portrait. Add matching keyboard controls for desktop.

## Rules and features

- Respawn invulnerability; extra points each level.
- Best score saved.

## Look and feel

- Type: Audiowide for display, system UI for body text
- Palette: background #05060a, text #f2f4ff, accent #7df9ff
- Layout: logical canvas 360×640, scaled to fit the screen
- A score/status strip at the top and a one-line control hint at the bottom. End-of-game and level-clear cards offer a clear next action (retry, next level, menu).
- Particles, small animations and screen feedback for hits, clears and wins. Keep motion purposeful.

## Technical requirements

- Render the playfield on a `<canvas>` at a fixed logical size, scaled to fit the available space with devicePixelRatio for sharpness. Clamp frame delta time (0 to 50 ms) so tab switches never break physics.
- Use pointer events for touch and mouse, with `touch-action: none` on the play area so the page never scrolls while playing.
- Respect safe-area insets (`env(safe-area-inset-*)`), keep at least a 16px side gutter, and never scroll horizontally at 360–400px widths.
- Save settings, unlocked levels, best scores and completed challenges in `localStorage`, wrapped in try/catch so the game still works when storage is blocked.
- No `alert()`/`confirm()`/`prompt()`; build any confirmation into the page.
- Test it: the game must load without console errors, start from the menu, and be playable start to finish.
