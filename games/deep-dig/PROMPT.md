# Prompt: Deep Dig

Paste the prompt below into Claude (or another capable coding model) to recreate this game as a single HTML file. Adjust anything you like before sending.

---

Build a complete, polished browser game called **Deep Dig**, inspired by Dig Dug, as **one self-contained HTML file** (inline CSS and JavaScript, no frameworks or build step; Google Fonts is the only allowed external resource, always with a system-font fallback). Use original characters and artwork drawn in code. Do not copy any trademarked characters, names or logos.

## The game

Tunnel through the earth and pump up monsters until they pop, or drop rocks on them. Fire-breathing lizards appear on later levels.

Menu text to show the player:

> Dig tunnels with the D-pad on one side and pop every monster. Face one and hold PUMP on the other side to inflate it until it bursts, or drop a rock on it for a big bonus. Move away to let go.

## Controls (phone first)

A D-pad on the left (hold to keep moving, slide to change direction) and a big PUMP button on the right; move and pump together. Hold the D-pad away for a moment to let go of a monster.

Touch must feel good on a phone held in portrait. Add matching keyboard controls for desktop.

## Rules and features

- 10 levels that unlock, and 7 challenges.
- A header mute button and pause button; the game pauses itself when you switch apps.

## Start menu settings

Show a start card with segmented buttons for each setting, remembered between visits:

- **Difficulty**: Easy, Normal, Hard
- **Lives**: 3, 5, 7
- **Pump**: Hold to pump, Tap each pump
- **Lizards breathe fire**: On, Off
- **Controls side**: Buttons right, Buttons left
- **Sound**: On, Off
- **Vibration**: On, Off

## Levels

10 levels that unlock in order, shown as a numbered grid with a lock icon on locked ones. The selected level's description appears under the grid:

1. Topsoil
2. Clay Pit
3. Rockfall
4. Fire Lizards
5. Deep Cut
6. Crowded Cave
7. Boulder Alley
8. Magma Run
9. Bedrock
10. Core Breaker

## Challenges

A collapsible checklist on the start card. When the player completes one, mark it done, save it, and show a short toast:

- Pop a monster
- Pop 5 monsters in one game
- Crush 2 monsters with one rock
- Pop a monster in the deepest layer
- Clear Rockfall (level 3)
- Clear a level without losing a life
- Clear Core Breaker (level 10)

## Look and feel

- Type: Luckiest Guy for display, system UI for body text
- Palette: background #170f0a, text #fff3df, accent #ffb92e
- Layout: logical canvas 364×442, scaled to fit the screen
- A score/status strip at the top and a one-line control hint at the bottom. End-of-game and level-clear cards offer a clear next action (retry, next level, menu).
- Particles, small animations and screen feedback for hits, clears and wins. Keep motion purposeful.

## Technical requirements

- Render the playfield on a `<canvas>` at a fixed logical size, scaled to fit the available space with devicePixelRatio for sharpness. Clamp frame delta time (0 to 50 ms) so tab switches never break physics.
- Use pointer events for touch and mouse, with `touch-action: none` on the play area so the page never scrolls while playing.
- Respect safe-area insets (`env(safe-area-inset-*)`), keep at least a 16px side gutter, and never scroll horizontally at 360–400px widths.
- Save settings, unlocked levels, best scores and completed challenges in `localStorage`, wrapped in try/catch so the game still works when storage is blocked.
- No `alert()`/`confirm()`/`prompt()`; build any confirmation into the page.
- Test it: the game must load without console errors, start from the menu, and be playable start to finish.
