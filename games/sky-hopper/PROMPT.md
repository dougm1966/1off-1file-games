# Prompt: Sky Hopper

Paste the prompt below into Claude (or another capable coding model) to recreate this game as a single HTML file. Adjust anything you like before sending.

---

Build a complete, polished browser game called **Sky Hopper**, inspired by Doodle Jump-style climber (original character), as **one self-contained HTML file** (inline CSS and JavaScript, no frameworks or build step; Google Fonts is the only allowed external resource, always with a system-font fallback). Use original characters and artwork drawn in code. Do not copy any trademarked characters, names or logos.

## The game

Bounce from platform to platform and climb as high as you can. Blue platforms slide, brown ones crack, white ones vanish after a bounce; springs, propeller hats and stompable gremlins.

Menu text to show the player:

> Bounce from platform to platform and climb as high as you can. Springs launch you, propeller hats fly you up, and you can stomp gremlins from above. Blue platforms slide, brown ones crack, white ones vanish after one bounce.

## Controls (phone first)

Slide left or right to steer; the hopper bounces automatically and wraps around the screen edges.

Touch must feel good on a phone held in portrait. Add matching keyboard controls for desktop.

## Start menu settings

Show a start card with segmented buttons for each setting, remembered between visits:

- **Difficulty**: Easy, Normal, Hard
- **Gremlins**: On, Off
- **Propeller hats**: On, Off
- **Hopper**: Blue, Orange, Mint

## Challenges

A collapsible checklist on the start card. When the player completes one, mark it done, save it, and show a short toast:

- Reach height 1,000
- Reach height 2,500
- Reach height 5,000
- Hit 5 springs in one run
- Grab a propeller hat
- Stomp a gremlin
- Collect 15 coins in one run

## Look and feel

- Type: Gochi Hand for display, system UI for body text
- Palette: background #fbf6e9, text #2b2a33, accent #3aa3ff
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
