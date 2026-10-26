# Prompt: Sunset Run

Paste the prompt below into Claude (or another capable coding model) to recreate this game as a single HTML file. Adjust anything you like before sending.

---

Build a complete, polished browser game called **Sunset Run**, inspired by OutRun-style pseudo-3D racing, as **one self-contained HTML file** (inline CSS and JavaScript, no frameworks or build step; Google Fonts is the only allowed external resource, always with a system-font fallback). Use original characters and artwork drawn in code. Do not copy any trademarked characters, names or logos.

## The game

Drive a red sports car down a winding desert highway at sunset, weaving through traffic and reaching checkpoints before the clock runs out.

## Controls (phone first)

Slide a finger left or right anywhere on the screen; the car follows the slide. Gas is automatic. Arrow keys also steer.

Touch must feel good on a phone held in portrait. Add matching keyboard controls for desktop.

## Rules and features

- Curves push the car outward; running off the asphalt slows you down.
- Each checkpoint adds time; traffic gets slightly faster as you go.
- Best distance is saved.

## Look and feel

- Type: Russo One + Chakra Petch
- Palette: synthwave sunset: purple-to-orange sky, striped sun, desert sand, red-and-white rumble strips, orange accent (#ffb238)
- Layout: full-screen canvas, horizon 30% down
- A score/status strip at the top and a one-line control hint at the bottom. End-of-game and level-clear cards offer a clear next action (retry, next level, menu).
- Particles, small animations and screen feedback for hits, clears and wins. Keep motion purposeful.

## Technical requirements

- Render the playfield on a `<canvas>` at a fixed logical size, scaled to fit the available space with devicePixelRatio for sharpness. Clamp frame delta time (0 to 50 ms) so tab switches never break physics.
- Use pointer events for touch and mouse, with `touch-action: none` on the play area so the page never scrolls while playing.
- Respect safe-area insets (`env(safe-area-inset-*)`), keep at least a 16px side gutter, and never scroll horizontally at 360–400px widths.
- Save settings, unlocked levels, best scores and completed challenges in `localStorage`, wrapped in try/catch so the game still works when storage is blocked.
- No `alert()`/`confirm()`/`prompt()`; build any confirmation into the page.
- Test it: the game must load without console errors, start from the menu, and be playable start to finish.
