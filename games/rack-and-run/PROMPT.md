# Prompt: Rack & Run

Paste the prompt below into Claude (or another capable coding model) to recreate this game as a single HTML file. Adjust anything you like before sending.

---

Build a complete, polished browser game called **Rack & Run**, inspired by 9-ball pool, as **one self-contained HTML file** (inline CSS and JavaScript, no frameworks or build step; Google Fonts is the only allowed external resource, always with a system-font fallback). Use original characters and artwork drawn in code. Do not copy any trademarked characters, names or logos.

## The game

Real 9-ball rules: hit the lowest-numbered ball first, pocket balls to keep shooting, legally pocket the 9 to win the rack. Fouls give the opponent ball in hand.

Menu text to show the player:

> Real 9-ball. Hit the lowest-numbered ball first. Sink anything legally to keep shooting. Legally pocket the 9 to win the rack. Fouls give your opponent ball in hand.

## Controls (phone first)

Slide on the table to rotate the cue, ‹ › to fine-tune, power slider, Shoot. During ball in hand, drag the cue ball, then tap Set ball.

Touch must feel good on a phone held in portrait. Add matching keyboard controls for desktop.

## Start menu settings

Show a start card with segmented buttons for each setting, remembered between visits:

- **Opponent**: Pass & play, CPU easy, CPU hard
- **Race to**: 3, 5, 7
- **Aim guide**: Full, Contact only, Short line
- **Break**: Alternate, Winner breaks

## Challenges

A collapsible checklist on the start card. When the player completes one, mark it done, save it, and show a short toast:

- Win a rack
- Break and run out a rack
- Make the 9 on the break
- Win a rack on a combo into the 9
- Win a race to 7
- Beat the hard CPU

## Look and feel

- Type: Bungee for display, system UI for body text
- Palette: background #0d1317, text #e9eef1, accent #d9a845
- Layout: logical canvas 452×812, scaled to fit the screen
- A score/status strip at the top and a one-line control hint at the bottom. End-of-game and level-clear cards offer a clear next action (retry, next level, menu).
- Particles, small animations and screen feedback for hits, clears and wins. Keep motion purposeful.

## Technical requirements

- Render the playfield on a `<canvas>` at a fixed logical size, scaled to fit the available space with devicePixelRatio for sharpness. Clamp frame delta time (0 to 50 ms) so tab switches never break physics.
- Use pointer events for touch and mouse, with `touch-action: none` on the play area so the page never scrolls while playing.
- Respect safe-area insets (`env(safe-area-inset-*)`), keep at least a 16px side gutter, and never scroll horizontally at 360–400px widths.
- Save settings, unlocked levels, best scores and completed challenges in `localStorage`, wrapped in try/catch so the game still works when storage is blocked.
- No `alert()`/`confirm()`/`prompt()`; build any confirmation into the page.
- Test it: the game must load without console errors, start from the menu, and be playable start to finish.
