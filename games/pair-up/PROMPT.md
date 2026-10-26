# Prompt: Pair Up

Paste the prompt below into Claude (or another capable coding model) to recreate this game as a single HTML file. Adjust anything you like before sending.

---

Build a complete, polished browser game called **Pair Up**, inspired by memory match / concentration, as **one self-contained HTML file** (inline CSS and JavaScript, no frameworks or build step; Google Fonts is the only allowed external resource, always with a system-font fallback). Use original characters and artwork drawn in code. Do not copy any trademarked characters, names or logos.

## The game

Flip two cards at a time to find pairs. Besides a lab-icon picture deck, three brainy decks match a term to its answer: tube color ↔ test, organism ↔ Gram stain, analyte ↔ normal range.

Menu text to show the player:

> Flip two cards at a time and find the pairs. The brainy decks match a term to its answer instead of identical pictures.

## Controls (phone first)

Tap two cards to flip them.

Touch must feel good on a phone held in portrait. Add matching keyboard controls for desktop.

## Start menu settings

Show a start card with segmented buttons for each setting, remembered between visits:

- **Deck**: Lab icons, Tube ↔ test, Bug ↔ Gram, Normal values
- **Players**: Solo, Two players
- **Peek at the start**: Off, 2 seconds
- **Flip-back speed**: Slow, Normal, Fast

## Levels

4 levels that unlock in order, shown as a numbered grid with a lock icon on locked ones. The selected level's description appears under the grid:

1. Warm-up 4×3
2. Classic 4×4
3. Big 4×5
4. Huge 5×6

## Challenges

A collapsible checklist on the start card. When the player completes one, mark it done, save it, and show a short toast:

- Finish with at most 2 extra moves
- Finish without a single miss
- Match 4 pairs in a row
- Clear the 4×4 in under 45 seconds
- Clear the 5×6 board
- Clear a level with a brainy deck
- Finish a two-player game

## Look and feel

- Type: Nunito for display, system UI for body text
- Palette: background #10233a, text #eef5fb, accent #4fd1c5
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
