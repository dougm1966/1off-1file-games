# Prompt: Tile Temple

Paste the prompt below into Claude (or another capable coding model) to recreate this game as a single HTML file. Adjust anything you like before sending.

---

Build a complete, polished browser game called **Tile Temple**, inspired by Mahjong solitaire, as **one self-contained HTML file** (inline CSS and JavaScript, no frameworks or build step; Google Fonts is the only allowed external resource, always with a system-font fallback). Use original characters and artwork drawn in code. Do not copy any trademarked characters, names or logos.

## The game

Match pairs of free tiles (not covered and open on the left or right) to clear stacked layouts.

Menu text to show the player:

> Mahjong solitaire. Clear the stack by matching identical pairs. A tile is free when nothing sits on it and its left or right side is open. Every deal can be solved.

## Controls (phone first)

Tap two matching free tiles.

Touch must feel good on a phone held in portrait. Add matching keyboard controls for desktop.

## Start menu settings

Show a start card with segmented buttons for each setting, remembered between visits:

- **Dim blocked tiles**: On, Off
- **Hints**: None, 3, Unlimited
- **Shuffles**: None, 1, 3

## Levels

4 levels that unlock in order, shown as a numbered grid with a lock icon on locked ones. The selected level's description appears under the grid:

1. Pyramid
2. Bridge
3. Twin towers
4. Diamond

## Challenges

A collapsible checklist on the start card. When the player completes one, mark it done, save it, and show a short toast:

- Clear any layout
- Clear without hints
- Clear in under 4 minutes
- Clear the Diamond
- Clear all four layouts

## Look and feel

- Type: Cinzel for display, system UI for body text
- Palette: background #1a2420, text #f3efe2, accent #e0b34f
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
