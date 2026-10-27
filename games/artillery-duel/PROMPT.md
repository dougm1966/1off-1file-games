# Prompt: Artillery Duel

Paste the prompt below into Claude (or another capable coding model) to recreate this game as a single HTML file. Adjust anything you like before sending.

---

Build a complete, polished browser game called **Artillery Duel**, inspired by turn-based artillery games, as **one self-contained HTML file** (inline CSS and JavaScript, no frameworks or build step; Google Fonts is the only allowed external resource, always with a system-font fallback). Use original characters and artwork drawn in code. Do not copy any trademarked characters, names or logos.

## The game

Turn-based tank artillery on destructible terrain, pass-and-play or against a CPU at three skill levels. Wind, six weapons, falling damage and limited fuel for moving.

Menu text to show the player:

> Tank duel on destructible ground. On your turn, drag back from your tank like a slingshot (the dotted arc shows the start of the shot) and let go to fire. Or use the AIM and POWER buttons and press FIRE. Mind the wind arrow. Wreck the other tank to win the round.

## Controls (phone first)

Drag back from your tank like a slingshot and let go to fire; a dotted arc shows the start of the shot. Or use the AIM, POWER, MOVE, WEAPON and FIRE buttons under the board.

Touch must feel good on a phone held in portrait. Add matching keyboard controls for desktop.

## Rules and features

- A pass card between turns in two-player games.
- A header mute button and pause button; the game pauses itself when you switch apps.

## Start menu settings

Show a start card with segmented buttons for each setting, remembered between visits:

- **Mode**: 2 players, CPU easy, CPU normal, CPU hard
- **Wind**: Off, Light, Wild
- **Terrain**: Random, Hills, Mountains, Canyon, Plateaus
- **Rounds**: 1, Best of 3, Best of 5
- **Weapons**: Shells only, Classic 3, Full arsenal
- **Tank fuel**: None, Some, Lots
- **Drag release**: Fires, Only aims
- **Aim arc**: Short, Long, Off
- **Controls side**: Buttons right, Buttons left
- **Sound**: On, Off
- **Vibration**: On, Off

## Challenges

A collapsible checklist on the start card. When the player completes one, mark it done, save it, and show a short toast:

- Win a round with a direct hit
- Win a round without taking damage
- Finish a tank with falling damage
- Finish a tank with a Roller
- Win a round in 3 shots or fewer
- Win a match in wild wind
- Beat the hard CPU in a match

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
