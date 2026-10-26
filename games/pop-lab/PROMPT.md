# Prompt: Pop Lab

Paste the prompt below into Claude (or another capable coding model) to recreate this game as a single HTML file. Adjust anything you like before sending.

---

Build a complete, polished browser game called **Pop Lab**, inspired by bubble shooter, as **one self-contained HTML file** (inline CSS and JavaScript, no frameworks or build step; Google Fonts is the only allowed external resource, always with a system-font fallback). Use original characters and artwork drawn in code. Do not copy any trademarked characters, names or logos.

## The game

Match three or more bubbles to pop them; anything left hanging falls for big points. Shots that don't pop anything push a new row down.

Menu text to show the player:

> Match three or more of a color to pop them. Anything left hanging falls off for big points. Every few shots that don't pop anything push a new row down.

## Controls (phone first)

Drag to aim, release to shoot; tap the spare bubble to swap.

Touch must feel good on a phone held in portrait. Add matching keyboard controls for desktop.

## Start menu settings

Show a start card with segmented buttons for each setting, remembered between visits:

- **Colors**: Fewer, By level, More
- **Aim guide**: Full + bounce, Short, Off
- **Row pressure**: Relaxed, Normal, Fast

## Levels

15 levels that unlock in order, shown as a numbered grid with a lock icon on locked ones. The selected level's description appears under the grid:

1. Warm-up · 3 colors
2. Pyramid
3. Stripes
4. Checkerboard · 4 colors
5. Hourglass
6. Islands
7. Deep rack · 5 colors
8. Zigzag
9. Hanging gardens
10. The wall
11. Diamonds · 6 colors
12. Pillars
13. Spiral-ish
14. Fortress
15. Final rack

## Challenges

A collapsible checklist on the start card. When the player completes one, mark it done, save it, and show a short toast:

- Drop 8+ bubbles with one shot
- Pop a group with a bank shot off the wall
- Clear a level before any new row
- Clear a level in 12 shots or fewer
- Clear level 10
- Clear all 15 levels

## Look and feel

- Type: Fredoka for display, system UI for body text
- Palette: background #10203a, text #eef6ff, accent #5ce1e6
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
