# Prompt: Puff Flight

Paste the prompt below into Claude (or another capable coding model) to recreate this game as a single HTML file. Adjust anything you like before sending.

---

Build a complete, polished browser game called **Puff Flight**, inspired by Flappy Bird-style flyer (original character), as **one self-contained HTML file** (inline CSS and JavaScript, no frameworks or build step; Google Fonts is the only allowed external resource, always with a system-font fallback). Use original characters and artwork drawn in code. Do not copy any trademarked characters, names or logos.

## The game

Tap to puff upward and glide through gaps. Grab coins; shield bubbles soak up one crash. From 10 points on, some pipes move.

Menu text to show the player:

> Tap to puff upward and glide through the gaps. Grab coins. Bubbles give you a shield that soaks up one crash. From 10 points on, some pipes start moving.

## Controls (phone first)

Tap anywhere (or space) to puff upward.

Touch must feel good on a phone held in portrait. Add matching keyboard controls for desktop.

## Start menu settings

Show a start card with segmented buttons for each setting, remembered between visits:

- **Difficulty**: Easy, Normal, Hard
- **World**: Meadow, Dusk, Clean room
- **Bird**: Sunny, Bubblegum, Lime
- **Shield bubbles**: On, Off

## Challenges

A collapsible checklist on the start card. When the player completes one, mark it done, save it, and show a short toast:

- Score 10
- Score 25
- Score 50
- Score 20 on Hard
- Grab 10 coins in one flight
- Squeak through 3 gaps by a feather

## Look and feel

- Type: Sniglet for display, system UI for body text
- Palette: background #7fd0f0, text #0f2b3d, accent #ff8a3d
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
