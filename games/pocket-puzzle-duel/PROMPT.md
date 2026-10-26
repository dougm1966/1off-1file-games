# Prompt: Pocket Puzzle Duel

Paste the prompt below into Claude (or another capable coding model) to recreate this game as a single HTML file. Adjust anything you like before sending.

---

Build a complete, polished browser game called **Pocket Puzzle Duel**, inspired by pool trick-shot puzzles, as **one self-contained HTML file** (inline CSS and JavaScript, no frameworks or build step; Google Fonts is the only allowed external resource, always with a system-font fallback). Use original characters and artwork drawn in code. Do not copy any trademarked characters, names or logos.

## The game

Two players take turns shooting the same pool table layout. Clear every ball in the fewest strokes, golf style, across six holes that add rails, bumper posts, a full rack and a gate of posts.

Menu text to show the player:

> Same table layout for both of you. Clear it in the fewest strokes. Lowest total after six holes wins.

## Controls (phone first)

Slide a finger left or right anywhere on the table to rotate the cue (it never snaps to your finger). ‹ › buttons fine-tune the angle. Set power with the slider and tap Shoot.

Touch must feel good on a phone held in portrait. Add matching keyboard controls for desktop.

## Rules and features

- Six holes with par values; a scratch costs +1 stroke; each hole has a stroke cap.
- The breaker alternates every hole; a hand-off screen says whose turn it is.
- Aim guide shows a dashed line to the first thing the cue ball touches plus a faint ghost ball, but not where balls go after contact.
- Match progress is saved between turns.

## Look and feel

- Type: Bungee (display) + Barlow / Barlow Condensed
- Palette: dark blue-green pool hall (#0d1317), tournament-blue cloth, walnut rails, brass accent (#d9a845)
- Layout: portrait canvas table 452×812
- A score/status strip at the top and a one-line control hint at the bottom. End-of-game and level-clear cards offer a clear next action (retry, next level, menu).
- Particles, small animations and screen feedback for hits, clears and wins. Keep motion purposeful.

## Technical requirements

- Render the playfield on a `<canvas>` at a fixed logical size, scaled to fit the available space with devicePixelRatio for sharpness. Clamp frame delta time (0 to 50 ms) so tab switches never break physics.
- Use pointer events for touch and mouse, with `touch-action: none` on the play area so the page never scrolls while playing.
- Respect safe-area insets (`env(safe-area-inset-*)`), keep at least a 16px side gutter, and never scroll horizontally at 360–400px widths.
- Save settings, unlocked levels, best scores and completed challenges in `localStorage`, wrapped in try/catch so the game still works when storage is blocked.
- No `alert()`/`confirm()`/`prompt()`; build any confirmation into the page.
- Test it: the game must load without console errors, start from the menu, and be playable start to finish.
