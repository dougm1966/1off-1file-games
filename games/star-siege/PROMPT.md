# Prompt: Star Siege

Paste the prompt below into Claude (or another capable coding model) to recreate this game as a single HTML file. Adjust anything you like before sending.

---

Build a complete, polished browser game called **Star Siege**, inspired by Space Invaders, as **one self-contained HTML file** (inline CSS and JavaScript, no frameworks or build step; Google Fonts is the only allowed external resource, always with a system-font fallback). Use original characters and artwork drawn in code. Do not copy any trademarked characters, names or logos.

## The game

Hold the line against marching alien ranks across 10 sectors, ending with a flagship boss. Shield bunkers wear down as they take hits.

Menu text to show the player:

> Hold the line against the descending fleet. Hold ◀ ▶ to move and the big FIRE button to shoot, at the same time. Shields soak shots but crumble. Hit the red saucer for bonus points.

## Controls (phone first)

◀ ▶ hold buttons on the left and a big FIRE button on the right; moving and firing at the same time works. Auto-fire is a setting. An alternative 'Drag ship' mode moves the ship by relative drag with auto-fire.

Touch must feel good on a phone held in portrait. Add matching keyboard controls for desktop.

## Rules and features

- 10 sectors that unlock, and 7 challenges.
- A header mute button and pause button; the game pauses itself when you switch apps.

## Start menu settings

Show a start card with segmented buttons for each setting, remembered between visits:

- **Difficulty**: Easy, Normal, Hard
- **Controls**: ◀ ▶ + FIRE, Drag ship
- **Auto-fire (buttons mode)**: Off, On
- **Lives**: 3, 5
- **Shield bunkers**: On, Off
- **Controls side**: Buttons right, Buttons left
- **Sound**: On, Off
- **Vibration**: On, Off

## Levels

10 levels that unlock in order, shown as a numbered grid with a lock icon on locked ones. The selected level's description appears under the grid:

1. First Contact
2. Scout Fleet
3. Full Armada
4. Raiders
5. Armored Ranks
6. Crossfire
7. Iron Wall
8. Low Orbit
9. Elite Guard
10. The Flagship

## Challenges

A collapsible checklist on the start card. When the player completes one, mark it done, save it, and show a short toast:

- Clear sector 1
- Shoot down the red saucer
- Hit 12 shots in a row without a miss
- Clear a sector without losing a ship
- Clear a sector in under 45 seconds
- Score 3000 points in one game
- Destroy the Flagship (sector 10)

## Look and feel

- Type: Orbitron for display, system UI for body text
- Palette: background #070b18, text #e6f0ff, accent #5cf2c4
- Layout: logical canvas 360×600, scaled to fit the screen
- A score/status strip at the top and a one-line control hint at the bottom. End-of-game and level-clear cards offer a clear next action (retry, next level, menu).
- Particles, small animations and screen feedback for hits, clears and wins. Keep motion purposeful.

## Technical requirements

- Render the playfield on a `<canvas>` at a fixed logical size, scaled to fit the available space with devicePixelRatio for sharpness. Clamp frame delta time (0 to 50 ms) so tab switches never break physics.
- Use pointer events for touch and mouse, with `touch-action: none` on the play area so the page never scrolls while playing.
- Respect safe-area insets (`env(safe-area-inset-*)`), keep at least a 16px side gutter, and never scroll horizontally at 360–400px widths.
- Save settings, unlocked levels, best scores and completed challenges in `localStorage`, wrapped in try/catch so the game still works when storage is blocked.
- No `alert()`/`confirm()`/`prompt()`; build any confirmation into the page.
- Test it: the game must load without console errors, start from the menu, and be playable start to finish.
