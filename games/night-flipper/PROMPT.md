# Prompt: Night Flipper

Paste the prompt below into Claude (or another capable coding model) to recreate this game as a single HTML file. Adjust anything you like before sending.

---

Build a complete, polished browser game called **Night Flipper**, inspired by pinball, as **one self-contained HTML file** (inline CSS and JavaScript, no frameworks or build step; Google Fonts is the only allowed external resource, always with a system-font fallback). Use original characters and artwork drawn in code. Do not copy any trademarked characters, names or logos.

## The game

A neon table with bumpers, slingshots, drop targets and top lanes. Rotating missions raise your multiplier and every second mission lights multiball.

Menu text to show the player:

> Keep the ball alive and work through the missions shown mid-table. Each one raises your multiplier. Every second mission lights multiball.

## Controls (phone first)

Hold the left or right half of the screen for each flipper (multi-touch). Hold, then release to launch; release at NOW for the skill shot.

Touch must feel good on a phone held in portrait. Add matching keyboard controls for desktop.

## Start menu settings

Show a start card with segmented buttons for each setting, remembered between visits:

- **Table slope**: Gentle, Standard, Steep
- **Balls**: 3, 5
- **Ball save**: Long, Short, Off
- **Multiball**: On, Off

## Challenges

A collapsible checklist on the start card. When the player completes one, mark it done, save it, and show a short toast:

- Hit the skill shot (release at NOW)
- Light all 3 top lanes
- Complete 3 missions in one game
- Complete 5 missions in one game
- Start multiball
- 100 bumper hits in one game
- Score 50,000
- Score 150,000

## Look and feel

- Type: Monoton for display, system UI for body text
- Palette: background #0b0618, text #fbefff, accent #ff4fd8
- Layout: logical canvas 340×640, scaled to fit the screen
- A score/status strip at the top and a one-line control hint at the bottom. End-of-game and level-clear cards offer a clear next action (retry, next level, menu).
- Particles, small animations and screen feedback for hits, clears and wins. Keep motion purposeful.

## Technical requirements

- Render the playfield on a `<canvas>` at a fixed logical size, scaled to fit the available space with devicePixelRatio for sharpness. Clamp frame delta time (0 to 50 ms) so tab switches never break physics.
- Use pointer events for touch and mouse, with `touch-action: none` on the play area so the page never scrolls while playing.
- Respect safe-area insets (`env(safe-area-inset-*)`), keep at least a 16px side gutter, and never scroll horizontally at 360–400px widths.
- Save settings, unlocked levels, best scores and completed challenges in `localStorage`, wrapped in try/catch so the game still works when storage is blocked.
- No `alert()`/`confirm()`/`prompt()`; build any confirmation into the page.
- Test it: the game must load without console errors, start from the menu, and be playable start to finish.
