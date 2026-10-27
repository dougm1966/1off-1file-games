# Prompt: Pantry Raid

Paste the prompt below into Claude (or another capable coding model) to recreate this game as a single HTML file. Adjust anything you like before sending.

---

Build a complete, polished browser game called **Pantry Raid**, inspired by Pac-Man, as **one self-contained HTML file** (inline CSS and JavaScript, no frameworks or build step; Google Fonts is the only allowed external resource, always with a system-font fallback). Use original characters and artwork drawn in code. Do not copy any trademarked characters, names or logos.

## The game

A mouse eats every crumb in the pantry while cats prowl. Cheese turns the tables. Three maze layouts, 2–4 cats, 10 levels.

Menu text to show the player:

> Sneak the mouse through the pantry and eat every crumb. Steer with the D-pad: press a direction early and the mouse turns at the next opening. Cheese makes the cats run, so chase them back to their box.

## Controls (phone first)

A D-pad under the board. Press a direction early and the mouse turns at the next opening; a small arrow on the mouse shows the waiting turn. Swipe on the board also works (setting).

Touch must feel good on a phone held in portrait. Add matching keyboard controls for desktop.

## Rules and features

- 10 levels that unlock, and 7 challenges.
- A header mute button and pause button; the game pauses itself when you switch apps.

## Start menu settings

Show a start card with segmented buttons for each setting, remembered between visits:

- **Maze**: Classic, Cellar, Shelves
- **Cats**: 2, 3, 4
- **Cat speed**: Slow, Normal, Fast
- **Lives**: 3, 5, 7
- **Swipe on board**: On, Off
- **Early turns**: Buffered, Instant only
- **Controls side**: Buttons right, Buttons left
- **Sound**: On, Off
- **Vibration**: On, Off

## Levels

10 levels that unlock in order, shown as a numbered grid with a lock icon on locked ones. The selected level's description appears under the grid:

1. Crumb Trail
2. Cheese Please
3. Cat Nap
4. Tail Tip
5. Midnight Snack
6. Pantry Patrol
7. Whisker Walk
8. Cat Cradle
9. Mouse Trap Alley
10. The Big Cheese

## Challenges

A collapsible checklist on the start card. When the player completes one, mark it done, save it, and show a short toast:

- Chase down 3 cats with one cheese
- Eat a bonus apple
- Clear a level without being caught
- Clear a level with Fast cats
- Score 5000 in one game
- Clear Midnight Snack (level 5)
- Clear The Big Cheese

## Look and feel

- Type: Chewy for display, system UI for body text
- Palette: background #1b1410, text #fff4e0, accent #ffcf4a
- Layout: logical canvas 342×378, scaled to fit the screen
- A score/status strip at the top and a one-line control hint at the bottom. End-of-game and level-clear cards offer a clear next action (retry, next level, menu).
- Particles, small animations and screen feedback for hits, clears and wins. Keep motion purposeful.

## Technical requirements

- Render the playfield on a `<canvas>` at a fixed logical size, scaled to fit the available space with devicePixelRatio for sharpness. Clamp frame delta time (0 to 50 ms) so tab switches never break physics.
- Use pointer events for touch and mouse, with `touch-action: none` on the play area so the page never scrolls while playing.
- Respect safe-area insets (`env(safe-area-inset-*)`), keep at least a 16px side gutter, and never scroll horizontally at 360–400px widths.
- Save settings, unlocked levels, best scores and completed challenges in `localStorage`, wrapped in try/catch so the game still works when storage is blocked.
- No `alert()`/`confirm()`/`prompt()`; build any confirmation into the page.
- Test it: the game must load without console errors, start from the menu, and be playable start to finish.
