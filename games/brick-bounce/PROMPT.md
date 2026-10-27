# Prompt: Brick Bounce

Paste the prompt below into Claude (or another capable coding model) to recreate this game as a single HTML file. Adjust anything you like before sending.

---

Build a complete, polished browser game called **Brick Bounce**, inspired by Breakout, as **one self-contained HTML file** (inline CSS and JavaScript, no frameworks or build step; Google Fonts is the only allowed external resource, always with a system-font fallback). Use original characters and artwork drawn in code. Do not copy any trademarked characters, names or logos.

## The game

Break every brick with the ball across 10 designed levels. Bricks take 1–3 hits; steel bricks need help, bombs clear their neighbours, and falling power-ups give a wide paddle, multi-ball, slow ball, catch or an extra life.

Menu text to show the player:

> Break every brick with the ball. Drag anywhere on the board to slide the paddle (the finger never has to touch it) and tap to launch. Catch falling capsules for power-ups.

## Controls (phone first)

Drag anywhere on the board: the paddle moves by however far your finger moves, so your finger never has to sit on the paddle or cover the ball. Tap to launch. A setting swaps to on-screen ◀ ▶ hold buttons and a LAUNCH button.

Touch must feel good on a phone held in portrait. Add matching keyboard controls for desktop.

## Rules and features

- 10 levels that unlock as you clear them, and 7 challenges.
- A header mute button and pause button; the game pauses itself when you switch apps.

## Start menu settings

Show a start card with segmented buttons for each setting, remembered between visits:

- **Difficulty**: Easy, Normal, Hard
- **Paddle control**: Drag (relative), Buttons
- **Drag sensitivity**: Low, Normal, High
- **Lives**: 3, 5, 7
- **Power-ups**: On, Off
- **Controls side**: Buttons right, Buttons left
- **Sound**: On, Off
- **Vibration**: On, Off

## Levels

10 levels that unlock in order, shown as a numbered grid with a lock icon on locked ones. The selected level's description appears under the grid:

1. First Bricks
2. Checkerboard
3. Pyramid
4. Hard Hats
5. Fortress
6. Pillars
7. Bombs Away
8. Diamond
9. Armor Plating
10. Brick Boss

## Challenges

A collapsible checklist on the start card. When the player completes one, mark it done, save it, and show a short toast:

- Clear a level
- Catch a Multi-ball capsule
- Break 8 bricks without touching the paddle
- Blow up a bomb brick
- Clear level 5 without losing a ball
- Score 5000 points in one game
- Clear Brick Boss (level 10)

## Look and feel

- Type: Righteous for display, system UI for body text
- Palette: background #14122b, text #f4f1ff, accent #ff8a3d
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
