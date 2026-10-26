# Prompt: Nine Squares

Paste the prompt below into Claude (or another capable coding model) to recreate this game as a single HTML file. Adjust anything you like before sending.

---

Build a complete, polished browser game called **Nine Squares**, inspired by Sudoku, as **one self-contained HTML file** (inline CSS and JavaScript, no frameworks or build step; Google Fonts is the only allowed external resource, always with a system-font fallback). Use original characters and artwork drawn in code. Do not copy any trademarked characters, names or logos.

## The game

Freshly generated Sudoku puzzles with exactly one solution, in four difficulties, with pencil notes, hints and undo.

Menu text to show the player:

> Fill the grid so every row, column and 3×3 box has 1 through 9 once. Every puzzle is freshly generated and has exactly one solution.

## Controls (phone first)

Tap a square, then a number. Notes mode adds pencil marks; Erase, Undo and Hint buttons.

Touch must feel good on a phone held in portrait. Add matching keyboard controls for desktop.

## Start menu settings

Show a start card with segmented buttons for each setting, remembered between visits:

- **Difficulty**: Easy, Medium, Hard, Expert
- **Show wrong numbers**: Red, Hidden
- **Mistake limit**: 3 strikes, Off
- **Hints**: None, 3, 9
- **Clear notes automatically**: On, Off

## Challenges

A collapsible checklist on the start card. When the player completes one, mark it done, save it, and show a short toast:

- Solve an Easy
- Solve a Medium
- Solve a Hard
- Solve an Expert
- Solve with zero mistakes
- Solve without hints
- Solve a Medium in under 10 minutes

## Look and feel

- Type: Fraunces for display, system UI for body text
- Palette: background #f4f0e8, text #22201c, accent #3b6ea8
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
