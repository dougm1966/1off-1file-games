# Prompt: Flow Lines

Paste the prompt below into Claude (or another capable coding model) to recreate this game as a single HTML file. Adjust anything you like before sending.

---

Build a complete, polished browser game called **Flow Lines**, inspired by pipe-connection puzzles, as **one self-contained HTML file** (inline CSS and JavaScript, no frameworks or build step; Google Fonts is the only allowed external resource, always with a system-font fallback). Use original characters and artwork drawn in code. Do not copy any trademarked characters, names or logos.

## The game

Rotate pipe tiles until every pipe connects back to the source. Classic, Timed flow (race the liquid) and a Daily puzzle, from 5×5 up to 9×11.

Menu text to show the player:

> Tap a tile to turn it a quarter turn, and hold a tile to lock it. Connect every pipe back to the orange source so the whole network lights up. In Timed flow, finish before the liquid arrives.

## Controls (phone first)

Tap a tile to rotate it 90°; long-press to lock it. Undo, Reset and Hint buttons under the board. Connected pipes light up.

Touch must feel good on a phone held in portrait. Add matching keyboard controls for desktop.

## Rules and features

- 11 size tiers that unlock, wrap-around edges and a colour-blind-friendly palette.
- A header mute button and pause button; the game pauses itself when you switch apps.

## Start menu settings

Show a start card with segmented buttons for each setting, remembered between visits:

- **Mode**: Classic, Timed flow, Daily
- **Board size**: Smaller, Tier size, Larger
- **Wrap-around edges**: Off, On
- **Colours**: Standard, Colour-blind friendly
- **Tap turns**: Clockwise, Counter-clockwise
- **Flow animation**: On, Off
- **Sound**: On, Off
- **Vibration**: On, Off

## Levels

11 levels that unlock in order, shown as a numbered grid with a lock icon on locked ones. The selected level's description appears under the grid:

1. Trickle · 5×5
2. Brook · 5×6
3. Stream · 6×6
4. Creek · 6×7
5. River · 7×7
6. Canal · 7×8
7. Delta · 8×8
8. Rapids · 8×9
9. Torrent · 9×9
10. Cascade · 9×10
11. Deluge · 9×11

## Challenges

A collapsible checklist on the start card. When the player completes one, mark it done, save it, and show a short toast:

- Solve any puzzle
- Solve in par moves or fewer
- Solve a 7×7 or larger board
- Solve a puzzle with wrap-around on
- Win a Timed flow puzzle
- Solve the daily puzzle
- Lock a tile with a long press

## Look and feel

- Type: system UI
- Palette: 
- Layout: 
- A score/status strip at the top and a one-line control hint at the bottom. End-of-game and level-clear cards offer a clear next action (retry, next level, menu).
- Particles, small animations and screen feedback for hits, clears and wins. Keep motion purposeful.

## Technical requirements

- Render the playfield on a `<canvas>` at a fixed logical size, scaled to fit the available space with devicePixelRatio for sharpness. Clamp frame delta time (0 to 50 ms) so tab switches never break physics.
- Use pointer events for touch and mouse, with `touch-action: none` on the play area so the page never scrolls while playing.
- Respect safe-area insets (`env(safe-area-inset-*)`), keep at least a 16px side gutter, and never scroll horizontally at 360–400px widths.
- Save settings, unlocked levels, best scores and completed challenges in `localStorage`, wrapped in try/catch so the game still works when storage is blocked.
- No `alert()`/`confirm()`/`prompt()`; build any confirmation into the page.
- Test it: the game must load without console errors, start from the menu, and be playable start to finish.
