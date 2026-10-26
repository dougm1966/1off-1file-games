# Prompt: Lily Pad Dash

Paste the prompt below into Claude (or another capable coding model) to recreate this game as a single HTML file. Adjust anything you like before sending.

---

Build a complete, polished browser game called **Lily Pad Dash**, inspired by Frogger, as **one self-contained HTML file** (inline CSS and JavaScript, no frameworks or build step; Google Fonts is the only allowed external resource, always with a system-font fallback). Use original characters and artwork drawn in code. Do not copy any trademarked characters, names or logos.

## The game

Hop a frog across five lanes of traffic and a river of logs and diving turtles into five lily-pad bays. Fill every bay to clear the level; speeds rise each level.

## Controls (phone first)

Tap ahead of the frog to hop forward, behind it to hop back, and beside it to hop left or right. Arrow keys also work.

Touch must feel good on a phone held in portrait. Add matching keyboard controls for desktop.

## Rules and features

- Three lives, a 30-second timer per frog, points for every new row reached and bonus points for time left.
- Turtles periodically dive; standing on a submerged turtle drops you in the river.

## Look and feel

- Type: Lilita One + Nunito
- Palette: deep green (#10241a) with a warm yellow accent (#ffd34d); bright cartoon cars, logs, red-shelled turtles
- Layout: canvas 360×520 on a 40px grid
- A score/status strip at the top and a one-line control hint at the bottom. End-of-game and level-clear cards offer a clear next action (retry, next level, menu).
- Particles, small animations and screen feedback for hits, clears and wins. Keep motion purposeful.

## Technical requirements

- Render the playfield on a `<canvas>` at a fixed logical size, scaled to fit the available space with devicePixelRatio for sharpness. Clamp frame delta time (0 to 50 ms) so tab switches never break physics.
- Use pointer events for touch and mouse, with `touch-action: none` on the play area so the page never scrolls while playing.
- Respect safe-area insets (`env(safe-area-inset-*)`), keep at least a 16px side gutter, and never scroll horizontally at 360–400px widths.
- Save settings, unlocked levels, best scores and completed challenges in `localStorage`, wrapped in try/catch so the game still works when storage is blocked.
- No `alert()`/`confirm()`/`prompt()`; build any confirmation into the page.
- Test it: the game must load without console errors, start from the menu, and be playable start to finish.
