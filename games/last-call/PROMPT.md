# Prompt: Last Call

Paste the prompt below into Claude (or another capable coding model) to recreate this game as a single HTML file. Adjust anything you like before sending.

---

Build a complete, polished browser game called **Last Call**, inspired by Tapper, as **one self-contained HTML file** (inline CSS and JavaScript, no frameworks or build step; Google Fonts is the only allowed external resource, always with a system-font fallback). Use original characters and artwork drawn in code. Do not copy any trademarked characters, names or logos.

## The game

Customers walk up four bars. Slide each a drink before they reach you, catch the empty mugs they send back and grab tips. Don't let a drink or mug fall off the end.

Menu text to show the player:

> Customers walk up the bars. Slide them a drink before they reach you. Catch the empty mugs they send back. Don't let a drink or a mug fall off the end.

## Controls (phone first)

Tap a bar to step behind it and slide a drink down it; tap coins to collect tips.

Touch must feel good on a phone held in portrait. Add matching keyboard controls for desktop.

## Start menu settings

Show a start card with segmented buttons for each setting, remembered between visits:

- **Pace**: Relaxed, Standard, Rush hour
- **Lives**: 3, 5
- **Shop**: Soda fountain, Coffee bar

## Levels

10 levels that unlock in order, shown as a numbered grid with a lock icon on locked ones. The selected level's description appears under the grid:

1. Round 1 · serve 8
2. Round 2 · serve 11
3. Round 3 · serve 14
4. Round 4 · serve 17
5. Round 5 · serve 20
6. Round 6 · serve 23
7. Round 7 · serve 26
8. Round 8 · serve 29
9. Round 9 · serve 32
10. Round 10 · serve 35

## Challenges

A collapsible checklist on the start card. When the player completes one, mark it done, save it, and show a short toast:

- Finish a round without losing a life
- Finish a round without breaking a glass
- Send 4 customers out the door within 5 seconds
- Collect 10 tips in total
- Clear round 5
- Clear round 10

## Look and feel

- Type: Shrikhand for display, system UI for body text
- Palette: background #1d0f0b, text #fff1e0, accent #ff9d3d
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
