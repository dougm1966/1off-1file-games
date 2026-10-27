# Prompt: Last Line

Paste the prompt below into Claude (or another capable coding model) to recreate this game as a single HTML file. Adjust anything you like before sending.

---

Build a complete, polished browser game called **Last Line**, inspired by Missile Command, as **one self-contained HTML file** (inline CSS and JavaScript, no frameworks or build step; Google Fonts is the only allowed external resource, always with a system-font fallback). Use original characters and artwork drawn in code. Do not copy any trademarked characters, names or logos.

## The game

Defend six cities from falling missiles, splitters and bombers across 10 waves, with limited interceptors at three bases.

Menu text to show the player:

> Missiles are falling on your six cities. Tap the exact spot in the sky where you want a counter-missile to burst. Blasts take a moment to grow, so lead your shots.

## Controls (phone first)

Tap the exact point in the sky where you want an interceptor to burst; a crosshair marks it and nothing is offset. Several fingers can tap at once. A 'Selected base' setting adds three base buttons to choose which base fires.

Touch must feel good on a phone held in portrait. Add matching keyboard controls for desktop.

## Rules and features

- 10 waves that unlock, and 7 challenges.
- A header mute button and pause button; the game pauses itself when you switch apps.

## Start menu settings

Show a start card with segmented buttons for each setting, remembered between visits:

- **Launch from**: Nearest base, Selected base
- **Difficulty**: Easy, Normal, Hard
- **Ammo per base**: 8, 10, 14
- **Blast size**: Normal, Large
- **Sound**: On, Off
- **Vibration**: On, Off

## Levels

10 levels that unlock in order, shown as a numbered grid with a lock icon on locked ones. The selected level's description appears under the grid:

1. First Strike
2. Sky Rain
3. Split Decision
4. Bomber Run
5. Night Raid
6. Swarm
7. Meteor Shower
8. Double Bombers
9. Firestorm
10. The Last Line

## Challenges

A collapsible checklist on the start card. When the player completes one, mark it done, save it, and show a short toast:

- Destroy 4 missiles with one interceptor
- Shoot down a bomber
- Clear a wave without losing a city or base
- Clear a wave with 15+ ammo left
- Clear Night Raid (wave 5)
- Score 5000 in one game
- Clear The Last Line (wave 10)

## Look and feel

- Type: Teko for display, system UI for body text
- Palette: background #0a0716, text #fff1e8, accent #ffcc33
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
