# Prompt: Curl & Shuffle

Paste the prompt below into Claude (or another capable coding model) to recreate this game as a single HTML file. Adjust anything you like before sending.

---

Build a complete, polished browser game called **Curl & Shuffle**, inspired by curling and table shuffleboard, as **one self-contained HTML file** (inline CSS and JavaScript, no frameworks or build step; Google Fonts is the only allowed external resource, always with a system-font fallback). Use original characters and artwork drawn in code. Do not copy any trademarked characters, names or logos.

## The game

Two games in one, pass-and-play or against a CPU: curling with ends, hammer and proper scoring, and table shuffleboard with 1-2-3 zones, hangers and knock-offs.

Menu text to show the player:

> Two games, one phone. Curling: drag back from the hack zone and release (angle sets the line, length sets the weight), pick IN or OUT curl, then hold SWEEP while the stone slides. Shuffleboard: flick a puck up the table. Play a friend, passing the phone, or the CPU.

## Controls (phone first)

Curling: pick IN or OUT curl, drag back from the hack and release to throw, and hold the big SWEEP button while the stone travels to carry it farther and straighter. Shuffleboard: flick the puck from the flick zone.

Touch must feel good on a phone held in portrait. Add matching keyboard controls for desktop.

## Rules and features

- A pass card between turns in two-player games.
- A header mute button and pause button; the game pauses itself when you switch apps.

## Start menu settings

Show a start card with segmented buttons for each setting, remembered between visits:

- **Game**: Curling, Shuffleboard
- **Mode**: vs CPU, 2 players
- **Curling: ends**: 2, 4, 6
- **Curling: stones each**: 4 (short), 8 (full)
- **Shuffleboard: target score**: 11, 15, 21
- **Ice / table speed**: Slow, Normal, Fast
- **CPU skill**: Easy, Normal, Hard
- **Controls side**: Buttons right, Buttons left
- **Sound**: On, Off
- **Vibration**: On, Off

## Challenges

A collapsible checklist on the start card. When the player completes one, mark it done, save it, and show a short toast:

- Sweep a stone into the house
- Land a stone on the button
- Knock an opposing stone out of play
- Score 2 or more in one curling end
- Win a curling match against the CPU
- Land a hanger in shuffleboard
- Win a shuffleboard match against the CPU

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
