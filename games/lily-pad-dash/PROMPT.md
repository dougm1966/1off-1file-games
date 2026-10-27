# Prompt: Lily Pad Dash

Paste the prompt below into Claude (or another capable coding model) to recreate this game as a single HTML file. Adjust anything you like before sending.

---

Build a complete, polished browser game called **Lily Pad Dash**, inspired by Frogger, as **one self-contained HTML file** (inline CSS and JavaScript, no frameworks or build step; Google Fonts is the only allowed external resource, always with a system-font fallback). Use original characters and artwork drawn in code. Do not copy any trademarked characters, names or logos.

## The game

Hop a frog across five lanes of traffic and a river of logs and diving turtles into five lily-pad bays. Fill every bay to clear the level. Ten levels add faster lanes, diving turtles and a gator.

Menu text to show the player:

> Hop across the road and river and fill all five lily pads. Use the D-pad under the board: each press is one square. You can also swipe on the board.

## Controls (phone first)

A D-pad under the board: each press is one hop in the direction of the wedge you touch, and the next square is outlined on the board. A big HOP button hops forward. You can also swipe on the board. Arrow keys work too.

Touch must feel good on a phone held in portrait. Add matching keyboard controls for desktop.

## Rules and features

- 10 levels that unlock, and 7 challenges.
- Settings include difficulty, lives, hold-to-keep-hopping and the grid guide.
- A header mute button and pause button; the game pauses itself when you switch apps.

## Start menu settings

Show a start card with segmented buttons for each setting, remembered between visits:

- **Difficulty**: Easy, Normal, Hard
- **Lives**: 3, 5, 7
- **Swipe on board**: On, Off
- **Tap board to hop forward**: On, Off
- **Hold to keep hopping**: Off, On
- **Grid guide**: On, Off
- **Controls side**: Buttons right, Buttons left
- **Sound**: On, Off
- **Vibration**: On, Off

## Levels

10 levels that unlock in order, shown as a numbered grid with a lock icon on locked ones. The selected level's description appears under the grid:

1. Pond Path
2. Morning Rush
3. Log Jam
4. Diving Turtles
5. Fast Lane
6. Flood Tide
7. Gator Bay
8. Night Traffic
9. Rapids
10. Lily Legend

## Challenges

A collapsible checklist on the start card. When the player completes one, mark it done, save it, and show a short toast:

- Eat a fly in a lily bay
- Reach a lily pad within 8 seconds
- Clear a level without losing a frog
- Clear Fast Lane (level 5)
- Clear level 3 on Hard
- Clear Lily Legend
- Make 500 hops in one game

## Look and feel

- Type: Lilita One + Nunito
- Palette: deep green (#10241a) with a warm yellow accent (#ffd34d); bright cartoon cars, logs, red-shelled turtles
- Layout: canvas 360×520 on a 40px grid
- A score/status strip at the top and a one-line control hint at the bottom. End-of-game and level-clear cards offer a clear next action (retry, next level, menu).
- Particles, small animations and screen feedback for hits, clears and wins. Keep motion purposeful.

## Technical requirements

- Render the playfield on a `<canvas>` at a fixed logical size, scaled to fit the available space with devicePixelRatio for sharpness. Clamp frame delta time (0 to 50 ms) so tab switches never break physics.
- Use pointer events for touch and mouse, with `touch-action: none` on the play area so the page never scrolls while playing.
- Respect safe-area insets (`env(safe-area-inset-*)`), keep at least a 16px side gutter, and never scroll horizontally at 360–400px widths.
- Save settings, unlocked levels, best scores and completed challenges in `localStorage`, wrapped in try/catch so the game still works when storage is blocked.
- No `alert()`/`confirm()`/`prompt()`; build any confirmation into the page.
- Test it: the game must load without console errors, start from the menu, and be playable start to finish.
