# Prompt: Sky Rescue

Paste the prompt below into Claude (or another capable coding model) to recreate this game as a single HTML file. Adjust anything you like before sending.

---

Build a complete, polished browser game called **Sky Rescue**, inspired by Defender, as **one self-contained HTML file** (inline CSS and JavaScript, no frameworks or build step; Google Fonts is the only allowed external resource, always with a system-font fallback). Use original characters and artwork drawn in code. Do not copy any trademarked characters, names or logos.

## The game

Side-scrolling rescue shooter over a wrap-around world: shoot landers carrying people, catch them as they fall and fly low to set them down. Landers that reach the top become fast mutants.

Menu text to show the player:

> Green landers are abducting people. Shoot a lander that's carrying someone, then catch them as they fall and fly low to set them down. If a lander reaches the top, it becomes a fast mutant.

## Controls (phone first)

Slide up/down to fly, slide left/right to speed up and turn; the laser fires while touching. BOMB clears the screen.

Touch must feel good on a phone held in portrait. Add matching keyboard controls for desktop.

## Start menu settings

Show a start card with segmented buttons for each setting, remembered between visits:

- **Difficulty**: Easy, Standard, Hard
- **Laser**: While touching, Always on

## Levels

10 levels that unlock in order, shown as a numbered grid with a lock icon on locked ones. The selected level's description appears under the grid:

1. Wave 1
2. Wave 2
3. Wave 3
4. Wave 4
5. Wave 5
6. Wave 6
7. Wave 7
8. Wave 8
9. Wave 9
10. Wave 10

## Challenges

A collapsible checklist on the start card. When the player completes one, mark it done, save it, and show a short toast:

- Catch a falling person
- Finish a wave without losing anyone
- Finish a wave without getting hit
- Take out 5+ enemies with one bomb
- Reach wave 5
- Score 20,000

## Look and feel

- Type: Audiowide for display, system UI for body text
- Palette: background #04030c, text #f0ecff, accent #3dffb0
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
