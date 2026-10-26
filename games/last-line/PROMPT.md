# Prompt: Last Line

Paste the prompt below into Claude (or another capable coding model) to recreate this game as a single HTML file. Adjust anything you like before sending.

---

Build a complete, polished browser game called **Last Line**, inspired by Missile Command, as **one self-contained HTML file** (inline CSS and JavaScript, no frameworks or build step; Google Fonts is the only allowed external resource, always with a system-font fallback). Use original characters and artwork drawn in code. Do not copy any trademarked characters, names or logos.

## The game

Defend six cities from falling missiles by bursting counter-missiles in the sky. Some missiles split later in the game.

Menu text to show the player:

> Missiles are falling on your six cities. Tap the sky to burst a counter-missile there. Lead your shots, because blasts take a moment to grow.
> The nearest base with ammo fires. Leftover ammo and surviving cities pay a bonus.

## Controls (phone first)

Tap the sky where you want a burst; the nearest base with ammo fires.

Touch must feel good on a phone held in portrait. Add matching keyboard controls for desktop.

## Rules and features

- Leftover ammo and surviving cities pay a bonus each wave.
- Game ends when every city is gone.

## Look and feel

- Type: Teko for display, system UI for body text
- Palette: background #0a0716, text #fff1e8, accent #ffcc33
- Layout: logical canvas 360×600, scaled to fit the screen
- A score/status strip at the top and a one-line control hint at the bottom. End-of-game and level-clear cards offer a clear next action (retry, next level, menu).
- Particles, small animations and screen feedback for hits, clears and wins. Keep motion purposeful.

## Technical requirements

- Render the playfield on a `<canvas>` at a fixed logical size, scaled to fit the available space with devicePixelRatio for sharpness. Clamp frame delta time (0 to 50 ms) so tab switches never break physics.
- Use pointer events for touch and mouse, with `touch-action: none` on the play area so the page never scrolls while playing.
- Respect safe-area insets (`env(safe-area-inset-*)`), keep at least a 16px side gutter, and never scroll horizontally at 360–400px widths.
- Save settings, unlocked levels, best scores and completed challenges in `localStorage`, wrapped in try/catch so the game still works when storage is blocked.
- No `alert()`/`confirm()`/`prompt()`; build any confirmation into the page.
- Test it: the game must load without console errors, start from the menu, and be playable start to finish.
