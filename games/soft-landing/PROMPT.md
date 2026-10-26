# Prompt: Soft Landing

Paste the prompt below into Claude (or another capable coding model) to recreate this game as a single HTML file. Adjust anything you like before sending.

---

Build a complete, polished browser game called **Soft Landing**, inspired by Lunar Lander, as **one self-contained HTML file** (inline CSS and JavaScript, no frameworks or build step; Google Fonts is the only allowed external resource, always with a system-font fallback). Use original characters and artwork drawn in code. Do not copy any trademarked characters, names or logos.

## The game

Set a lander down gently on a lit pad. Come in slow and level; ×2/×3/×5 pads and stronger gravity pay more.

Menu text to show the player:

> Set the lander down gently on a lit pad. Come in slow and level. Higher-multiplier pads and stronger gravity pay more.

## Controls (phone first)

Hold anywhere to fire the engine; slide while holding to tilt.

Touch must feel good on a phone held in portrait. Add matching keyboard controls for desktop.

## Start menu settings

Show a start card with segmented buttons for each setting, remembered between visits:

- **Gravity**: Moon, Mars, Earth
- **Fuel**: Generous, Standard, Tight
- **Wind**: Off, By level, Always

## Levels

10 levels that unlock in order, shown as a numbered grid with a lock icon on locked ones. The selected level's description appears under the grid:

1. Wide pads, calm sky
2. Rolling hills
3. Two pads, one tight
4. Light crosswind
5. Jagged ridge
6. Narrow canyon
7. Gusty wind
8. Tiny ×5 ledge
9. Storm front
10. The needle

## Challenges

A collapsible checklist on the start card. When the player completes one, mark it done, save it, and show a short toast:

- Land on a ×5 pad
- Touch down under 10 px/s
- Land with over half your fuel left
- Land in Earth gravity
- Land without tilting at all
- Clear level 10

## Look and feel

- Type: Oxanium for display, system UI for body text
- Palette: background #05070d, text #e8f0ff, accent #ffd166
- Layout: logical canvas 360×640, scaled to fit the screen
- A score/status strip at the top and a one-line control hint at the bottom. End-of-game and level-clear cards offer a clear next action (retry, next level, menu).
- Particles, small animations and screen feedback for hits, clears and wins. Keep motion purposeful.

## Technical requirements

- Render the playfield on a `<canvas>` at a fixed logical size, scaled to fit the available space with devicePixelRatio for sharpness. Clamp frame delta time (0 to 50 ms) so tab switches never break physics.
- Use pointer events for touch and mouse, with `touch-action: none` on the play area so the page never scrolls while playing.
- Respect safe-area insets (`env(safe-area-inset-*)`), keep at least a 16px side gutter, and never scroll horizontally at 360–400px widths.
- Save settings, unlocked levels, best scores and completed challenges in `localStorage`, wrapped in try/catch so the game still works when storage is blocked.
- No `alert()`/`confirm()`/`prompt()`; build any confirmation into the page.
- Test it: the game must load without console errors, start from the menu, and be playable start to finish.
