# Prompt: Gem Rush

Paste the prompt below into Claude (or another capable coding model) to recreate this game as a single HTML file. Adjust anything you like before sending.

---

Build a complete, polished browser game called **Gem Rush**, inspired by match-3 gem games, as **one self-contained HTML file** (inline CSS and JavaScript, no frameworks or build step; Google Fonts is the only allowed external resource, always with a system-font fallback). Use original characters and artwork drawn in code. Do not copy any trademarked characters, names or logos.

## The game

Swap neighbouring gems to line up three or more. Four in a row makes a striped gem, an L or T makes a bomb, five makes a rainbow gem; levels have score or collect goals within a move limit.

Menu text to show the player:

> Swap neighboring gems to line up three or more. Match 4 for a striped gem that clears a line, an L or T for a bomb, and 5 for a rainbow gem that clears one whole color.

## Controls (phone first)

Swipe a gem into a neighbour to swap.

Touch must feel good on a phone held in portrait. Add matching keyboard controls for desktop.

## Start menu settings

Show a start card with segmented buttons for each setting, remembered between visits:

- **Gem colors**: 5 · easier, 6, 7 · harder
- **Moves**: +6, Standard, −4
- **Hints when idle**: On, Off
- **Animation**: Fast, Normal, Slow

## Levels

15 levels that unlock in order, shown as a numbered grid with a lock icon on locked ones. The selected level's description appears under the grid:

1. Score 2400
2. Score 3300
3. Collect 18 green
4. Score 5100
5. Score 6000
6. Collect 24 red
7. Score 7800
8. Score 8700
9. Collect 30 green
10. Score 10500
11. Score 11400
12. Collect 36 red
13. Score 13200
14. Score 14100
15. Collect 42 green

## Challenges

A collapsible checklist on the start card. When the player completes one, mark it done, save it, and show a short toast:

- Make a bomb gem
- Make a rainbow gem
- Chain a 5× cascade
- Clear a level with 5+ moves left
- Clear all 15 levels

## Look and feel

- Type: Baloo 2 for display, system UI for body text
- Palette: background #170d2b, text #f7f0ff, accent #ff7ad9
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
