# Prompt: Swarm Wing

Paste the prompt below into Claude (or another capable coding model) to recreate this game as a single HTML file. Adjust anything you like before sending.

---

Build a complete, polished browser game called **Swarm Wing**, inspired by Galaga, as **one self-contained HTML file** (inline CSS and JavaScript, no frameworks or build step; Google Fonts is the only allowed external resource, always with a system-font fallback). Use original characters and artwork drawn in code. Do not copy any trademarked characters, names or logos.

## The game

A swarm loops in on curved paths, forms up, then peels off to dive at your twin-cannon fighter. Hits during a dive score double; pink leaders take two hits.

Menu text to show the player:

> The swarm loops in, forms up, then peels off to dive at you. Hits during a dive score double.
> Slide anywhere to move. Twin cannons fire on their own. Pink leaders take two hits.

## Controls (phone first)

Slide anywhere to move; twin cannons fire automatically.

Touch must feel good on a phone held in portrait. Add matching keyboard controls for desktop.

## Rules and features

- Three lives, waves get faster.
- Best score saved.

## Look and feel

- Type: Exo 2 for display, system UI for body text
- Palette: background #06040f, text #f1ecff, accent #ffd23f
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
