# Prompt: Cube Hop

Paste the prompt below into Claude (or another capable coding model) to recreate this game as a single HTML file. Adjust anything you like before sending.

---

Build a complete, polished browser game called **Cube Hop**, inspired by Q*bert, as **one self-contained HTML file** (inline CSS and JavaScript, no frameworks or build step; Google Fonts is the only allowed external resource, always with a system-font fallback). Use original characters and artwork drawn in code. Do not copy any trademarked characters, names or logos.

## The game

Hop down a pyramid of cubes changing their colour while bouncing balls and a chaser come after you. Later levels flip cubes back when you land again. Escape discs carry you to the top.

Menu text to show the player:

> Hop on every cube until its top matches the goal colour. Use the four diamond buttons under the board: each arrow points the way you hop (keys Q W A S). You can also tap a glowing cube. Dodge red balls and the burr, and don't hop off the edge. Hop onto a spinning disc to ride it to the top.

## Controls (phone first)

Four diagonal buttons (↖ ↗ ↙ ↘) under the board, pointing the same way the hops go on the pyramid. You can also tap one of the highlighted neighbouring cubes. Keys Q W A S or arrows.

Touch must feel good on a phone held in portrait. Add matching keyboard controls for desktop.

## Rules and features

- 10 levels that unlock, and 7 challenges.
- A header mute button and pause button; the game pauses itself when you switch apps.

## Start menu settings

Show a start card with segmented buttons for each setting, remembered between visits:

- **Difficulty**: Easy, Normal, Hard
- **Lives**: 3, 5, 7
- **Escape discs**: On, Off
- **Tap a cube to hop**: On, Off
- **Hold button to keep hopping**: Off, On
- **Glow on hop targets**: On, Off
- **Sound**: On, Off
- **Vibration**: On, Off

## Levels

10 levels that unlock in order, shown as a numbered grid with a lock icon on locked ones. The selected level's description appears under the grid:

1. First Hops
2. Rolling Reds
3. Burr Alert
4. Double Colour
5. Two-Tone Trouble
6. Flip Flop
7. Flip and Flee
8. Burr Pair
9. Fast Flip
10. Summit Rush

## Challenges

A collapsible checklist on the start card. When the player completes one, mark it done, save it, and show a short toast:

- Clear Burr Alert (level 3)
- Clear Flip Flop (level 6)
- Clear Summit Rush (level 10)
- Ride an escape disc
- Sweep a burr off with a disc
- Clear a level without losing a life
- Score 5000 in one game

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
