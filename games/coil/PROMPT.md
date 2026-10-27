# Prompt: Coil

Paste the prompt below into Claude (or another capable coding model) to recreate this game as a single HTML file. Adjust anything you like before sending.

---

Build a complete, polished browser game called **Coil**, inspired by Snake, as **one self-contained HTML file** (inline CSS and JavaScript, no frameworks or build step; Google Fonts is the only allowed external resource, always with a system-font fallback). Use original characters and artwork drawn in code. Do not copy any trademarked characters, names or logos.

## The game

Grow the snake by eating apples without hitting walls, rocks or yourself. Classic, Obstacles and Timed modes, three board sizes, and solid or wrap-around walls.

Menu text to show the player:

> Eat apples to grow without hitting walls, rocks or yourself. Press the D-pad to turn (roll your thumb between directions; two quick turns are remembered). Golden stars are worth 50 but vanish fast.

## Controls (phone first)

A D-pad under the board: press a wedge to turn that way, or slide your thumb from wedge to wedge. Up to two quick turns are remembered, and a reversal into yourself is ignored. Hold BOOST to speed up. Swipe on the board is an optional setting.

Touch must feel good on a phone held in portrait. Add matching keyboard controls for desktop.

## Rules and features

- 7 challenges.
- A header mute button and pause button; the game pauses itself when you switch apps.

## Start menu settings

Show a start card with segmented buttons for each setting, remembered between visits:

- **Mode**: Classic, Obstacles, Timed
- **Speed**: Slow, Normal, Fast
- **Walls**: Solid, Wrap around
- **Board size**: Small, Medium, Large
- **Swipe on board (extra)**: Off, On
- **Controls side**: Buttons right, Buttons left
- **Sound**: On, Off
- **Vibration**: On, Off

## Challenges

A collapsible checklist on the start card. When the player completes one, mark it done, save it, and show a short toast:

- Grow to length 20
- Grow to length 40
- Eat a golden star
- Buffer two quick turns in a row
- Eat 10 apples with wrap-around walls
- Eat 8 apples in Obstacles mode
- Eat 15 apples in Timed mode

## Look and feel

- Type: Silkscreen for display, system UI for body text
- Palette: background #0f1a12, text #e8f5e1, accent #b8f05a
- Layout: logical canvas 360×504, scaled to fit the screen
- A score/status strip at the top and a one-line control hint at the bottom. End-of-game and level-clear cards offer a clear next action (retry, next level, menu).
- Particles, small animations and screen feedback for hits, clears and wins. Keep motion purposeful.

## Technical requirements

- Render the playfield on a `<canvas>` at a fixed logical size, scaled to fit the available space with devicePixelRatio for sharpness. Clamp frame delta time (0 to 50 ms) so tab switches never break physics.
- Use pointer events for touch and mouse, with `touch-action: none` on the play area so the page never scrolls while playing.
- Respect safe-area insets (`env(safe-area-inset-*)`), keep at least a 16px side gutter, and never scroll horizontally at 360–400px widths.
- Save settings, unlocked levels, best scores and completed challenges in `localStorage`, wrapped in try/catch so the game still works when storage is blocked.
- No `alert()`/`confirm()`/`prompt()`; build any confirmation into the page.
- Test it: the game must load without console errors, start from the menu, and be playable start to finish.
