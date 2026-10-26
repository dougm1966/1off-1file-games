# Prompt: Lab Hunt

Paste the prompt below into Claude (or another capable coding model) to recreate this game as a single HTML file. Adjust anything you like before sending.

---

Build a complete, polished browser game called **Lab Hunt**, inspired by word search, as **one self-contained HTML file** (inline CSS and JavaScript, no frameworks or build step; Google Fonts is the only allowed external resource, always with a system-font fallback). Use original characters and artwork drawn in code. Do not copy any trademarked characters, names or logos.

## The game

Word search with lab and medical word lists; find every hidden word in the grid.

Menu text to show the player:

> Find every lab word hidden in the grid. Each theme you finish unlocks the next.

## Controls (phone first)

Drag across letters in a straight line to select a word.

Touch must feel good on a phone held in portrait. Add matching keyboard controls for desktop.

## Start menu settings

Show a start card with segmented buttons for each setting, remembered between visits:

- **Grid**: 10×10 · across & down, 12×12 · + diagonals, 14×14 · + backwards
- **Timer**: On, Off

## Levels

8 levels that unlock in order, shown as a numbered grid with a lock icon on locked ones. The selected level's description appears under the grid:

1. Hematology
2. Lab gear
3. Chemistry
4. Microbiology
5. Coagulation
6. Urinalysis
7. Blood bank
8. Lab life

## Challenges

A collapsible checklist on the start card. When the player completes one, mark it done, save it, and show a short toast:

- Finish a theme
- Finish without hints
- Finish in under 2 minutes
- Find a backwards word
- Finish a 14×14 grid
- Finish all 8 themes

## Look and feel

- Type: Archivo Black for display, system UI for body text
- Palette: background #eef3f6, text #16232e, accent #d94c6a
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
