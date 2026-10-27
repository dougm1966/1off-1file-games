# Prompt: Kart Dash

Paste the prompt below into Claude (or another capable coding model) to recreate this game as a single HTML file. Adjust anything you like before sending.

---

Build a complete, polished browser game called **Kart Dash**, inspired by kart racing, as **one self-contained HTML file** (inline CSS and JavaScript, no frameworks or build step; Google Fonts is the only allowed external resource, always with a system-font fallback). Use original characters and artwork drawn in code. Do not copy any trademarked characters, names or logos.

## The game

Top-down kart racing against CPU karts across 9 tracks in 3 cups, with item boxes and drift boosts.

Menu text to show the player:

> Race five CPU karts for three laps. Hold ◀ ▶ to steer and GAS to go. Hold DRIFT while turning to slide: blue sparks give a small boost, orange sparks a big one when you let go. Tap the ITEM box on screen to use what you picked up from the ? boxes.

## Controls (phone first)

◀ ▶ hold buttons on the left; GAS and BRAKE/DRIFT on the right. Hold DRIFT while turning to build a boost, release to fire it. Tap the ITEM box to use an item. Drag-to-steer is a setting.

Touch must feel good on a phone held in portrait. Add matching keyboard controls for desktop.

## Rules and features

- Three CPU difficulties, saved best laps and an optional ghost of your best lap.
- A header mute button and pause button; the game pauses itself when you switch apps.

## Start menu settings

Show a start card with segmented buttons for each setting, remembered between visits:

- **CPU difficulty**: Easy, Normal, Hard
- **Mode**: Single race, Cup (3 races)
- **Laps**: 2, 3, 5
- **Steering**: ◀ ▶ buttons, Drag on board
- **Gas**: Hold GAS, Auto-gas
- **Item boxes**: On, Off
- **Ghost of best lap**: Off, On
- **Controls side**: Buttons right, Buttons left
- **Sound**: On, Off
- **Vibration**: On, Off

## Levels

9 levels that unlock in order, shown as a numbered grid with a lock icon on locked ones. The selected level's description appears under the grid:

1. Sunny Loop · Nut Cup
2. Figure Bay · Nut Cup
3. Pine Hairpin · Nut Cup
4. Canyon Run · Gear Cup
5. Harbor Chicane · Gear Cup
6. Peak Pass · Gear Cup
7. Neon Docks · Star Cup
8. Glacier Switch · Star Cup
9. Grand Circuit · Star Cup

## Challenges

A collapsible checklist on the start card. When the player completes one, mark it done, save it, and show a short toast:

- 1. Sunny Loop: lap --
- 2. Figure Bay: lap --
- 3. Pine Hairpin: lap --
- 4. Canyon Run: lap --
- 5. Harbor Chicane: lap --
- 6. Peak Pass: lap --
- 7. Neon Docks: lap --
- 8. Glacier Switch: lap --
- 9. Grand Circuit: lap --
- Win a race
- Release an orange-spark drift boost
- Hit a rival with a Seeker
- Finish on the podium without touching a wall
- Win after being in last place
- Win a cup
- Win a race on Hard

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
