# Prompt: Strike Lane

Paste the prompt below into Claude (or another capable coding model) to recreate this game as a single HTML file. Adjust anything you like before sending.

---

Build a complete, polished browser game called **Strike Lane**, inspired by ten-pin bowling, as **one self-contained HTML file** (inline CSS and JavaScript, no frameworks or build step; Google Fonts is the only allowed external resource, always with a system-font fallback). Use original characters and artwork drawn in code. Do not copy any trademarked characters, names or logos.

## The game

Ten-pin bowling for 1–4 players or against a CPU, with real pin physics and full scoring including strikes, spares and the 10th frame.

Menu text to show the player:

> Drag in the position strip to slide the bowler along the foul line. Then flick up from the release zone: the direction of the flick is your aim, its speed is your power, and a curve at the end of the flick adds hook. Ten pins, ten frames.

## Controls (phone first)

Drag the strip under the lane to slide the bowler along the foul line, then flick up from the release zone: flick direction aims, speed sets power, and a curve at the end of the flick adds hook.

Touch must feel good on a phone held in portrait. Add matching keyboard controls for desktop.

## Rules and features

- Oil patterns, ball weight, aim guide and a scorecard; a pass card between players.
- A header mute button and pause button; the game pauses itself when you switch apps.

## Start menu settings

Show a start card with segmented buttons for each setting, remembered between visits:

- **Players (pass and play)**: 1, 2, 3, 4
- **CPU opponent**: Off, Casual, Skilled, Pro
- **Oil pattern**: Dry, House, Slick
- **Ball weight**: 8 lb, 12 lb, 15 lb
- **Game length**: 10 frames, 5 frames
- **Aim guide while flicking**: On, Off
- **Show last throw path**: On, Off
- **Sound**: On, Off
- **Vibration**: On, Off

## Challenges

A collapsible checklist on the start card. When the player completes one, mark it done, save it, and show a short toast:

- Throw a strike
- Pick up a spare
- Three strikes in a row
- Strike with a strong hook
- Convert a split
- Score 150 or more in a game
- Beat the CPU

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
