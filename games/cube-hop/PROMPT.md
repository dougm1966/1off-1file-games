# Prompt: Cube Hop

Paste the prompt below into Claude (or another capable coding model) to recreate this game as a single HTML file. Adjust anything you like before sending.

---

Build a complete, polished browser game called **Cube Hop**, inspired by Q*bert-style pyramid hopping (original characters), as **one self-contained HTML file** (inline CSS and JavaScript, no frameworks or build step; Google Fonts is the only allowed external resource, always with a system-font fallback). Use original characters and artwork drawn in code. Do not copy any trademarked characters, names or logos.

## The game

Hop on every cube of a pyramid to change its top color; later levels need two hits or toggle back. Dodge bouncing red balls and a green burr that hunts you, and don't hop off the edge.

Menu text to show the player:

> Hop on every cube until all the tops match the goal color shown up top. Dodge the red balls and the green burr that hunts you. Don't hop off the edge.
> Tap above-left, above-right, below-left or below-right of the hopper to jump that way.

## Controls (phone first)

Tap diagonally around the hopper (above-left, above-right, below-left, below-right) to jump that way.

Touch must feel good on a phone held in portrait. Add matching keyboard controls for desktop.

## Rules and features

- Three lives; level clear bonus.
- Best score saved.

## Look and feel

- Type: Baloo 2 for display, system UI for body text
- Palette: background #101433, text #f1f3ff, accent #ffcf33
- Layout: logical canvas 360×560, scaled to fit the screen
- A score/status strip at the top and a one-line control hint at the bottom. End-of-game and level-clear cards offer a clear next action (retry, next level, menu).
- Particles, small animations and screen feedback for hits, clears and wins. Keep motion purposeful.

## Technical requirements

- Render the playfield on a `<canvas>` at a fixed logical size, scaled to fit the available space with devicePixelRatio for sharpness. Clamp frame delta time (0 to 50 ms) so tab switches never break physics.
- Use pointer events for touch and mouse, with `touch-action: none` on the play area so the page never scrolls while playing.
- Respect safe-area insets (`env(safe-area-inset-*)`), keep at least a 16px side gutter, and never scroll horizontally at 360–400px widths.
- Save settings, unlocked levels, best scores and completed challenges in `localStorage`, wrapped in try/catch so the game still works when storage is blocked.
- No `alert()`/`confirm()`/`prompt()`; build any confirmation into the page.
- Test it: the game must load without console errors, start from the menu, and be playable start to finish.
