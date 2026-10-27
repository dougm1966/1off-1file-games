# Prompt: Rock Field

Paste the prompt below into Claude (or another capable coding model) to recreate this game as a single HTML file. Adjust anything you like before sending.

---

Build a complete, polished browser game called **Rock Field**, inspired by Asteroids, as **one self-contained HTML file** (inline CSS and JavaScript, no frameworks or build step; Google Fonts is the only allowed external resource, always with a system-font fallback). Use original characters and artwork drawn in code. Do not copy any trademarked characters, names or logos.

## The game

Pilot a vector ship through 10 increasingly dangerous rock fields, splitting big rocks into small ones and dodging saucers.

Menu text to show the player:

> Blast the drifting rocks. Push the stick the way you want to fly: the ship turns to face it and thrusts harder the further you push. Hold FIRE to shoot. HYPER jumps to a random spot, with a risk.

## Controls (phone first)

A thumb stick on the left: the ship turns to face the stick and thrusts harder the further you push. FIRE (hold to repeat) and HYPER buttons on the right; steering and firing work together. A 'Classic buttons' setting gives ⟲ ⟳ THRUST instead.

Touch must feel good on a phone held in portrait. Add matching keyboard controls for desktop.

## Rules and features

- 10 levels that unlock, and 7 challenges.
- A header mute button and pause button; the game pauses itself when you switch apps.

## Start menu settings

Show a start card with segmented buttons for each setting, remembered between visits:

- **Controls**: Stick + Fire, Classic buttons
- **Difficulty**: Easy, Normal, Hard
- **Ships**: 3, 5
- **Saucers**: On, Off
- **Controls side**: Buttons right, Buttons left
- **Sound**: On, Off
- **Vibration**: On, Off

## Levels

10 levels that unlock in order, shown as a numbered grid with a lock icon on locked ones. The selected level's description appears under the grid:

1. Debris Drift
2. Gravel Run
3. Boulder Belt
4. Saucer Sighting
5. Crystal Cluster
6. Meteor Alley
7. Hot Rocks
8. Dust Storm
9. Iron Rain
10. The Last Field

## Challenges

A collapsible checklist on the start card. When the player completes one, mark it done, save it, and show a short toast:

- Shatter 6 rocks within 10 seconds
- Shoot down a saucer
- Clear a level without losing a ship
- Survive 3 hyperspace jumps in one game
- Score 3000 in one game
- Clear Crystal Cluster (level 5)
- Clear The Last Field

## Look and feel

- Type: Audiowide for display, system UI for body text
- Palette: background #05060a, text #f2f4ff, accent #7df9ff
- Layout: logical canvas 360×640, scaled to fit the screen
- A score/status strip at the top and a one-line control hint at the bottom. End-of-game and level-clear cards offer a clear next action (retry, next level, menu).
- Particles, small animations and screen feedback for hits, clears and wins. Keep motion purposeful.

## Technical requirements

- Render the playfield on a `<canvas>` at a fixed logical size, scaled to fit the available space with devicePixelRatio for sharpness. Clamp frame delta time (0 to 50 ms) so tab switches never break physics.
- Use pointer events for touch and mouse, with `touch-action: none` on the play area so the page never scrolls while playing.
- Respect safe-area insets (`env(safe-area-inset-*)`), keep at least a 16px side gutter, and never scroll horizontally at 360–400px widths.
- Save settings, unlocked levels, best scores and completed challenges in `localStorage`, wrapped in try/catch so the game still works when storage is blocked.
- No `alert()`/`confirm()`/`prompt()`; build any confirmation into the page.
- Test it: the game must load without console errors, start from the menu, and be playable start to finish.
