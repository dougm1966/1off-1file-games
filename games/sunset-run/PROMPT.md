# Prompt: Sunset Run

Paste the prompt below into Claude (or another capable coding model) to recreate this game as a single HTML file. Adjust anything you like before sending.

---

Build a complete, polished browser game called **Sunset Run**, inspired by Out Run, as **one self-contained HTML file** (inline CSS and JavaScript, no frameworks or build step; Google Fonts is the only allowed external resource, always with a system-font fallback). Use original characters and artwork drawn in code. Do not copy any trademarked characters, names or logos.

## The game

A pseudo-3D desert drive at sunset: weave through traffic and reach each checkpoint before the clock runs out, over 10 stages or in endless mode.

Menu text to show the player:

> Race the clock through the desert at sunset. Drag a finger sideways anywhere on the road to steer; the car follows your finger and the gas is automatic. Hold BRAKE to slow down. Pass each checkpoint to add time, and weave around traffic.

## Controls (phone first)

Drag sideways anywhere on the board and the car follows smoothly; gas is automatic and a BRAKE button sits on the right. A setting gives ◀ ▶ GAS BRAKE buttons instead.

Touch must feel good on a phone held in portrait. Add matching keyboard controls for desktop.

## Rules and features

- 10 stages that unlock, and 8 challenges.
- A header mute button and pause button; the game pauses itself when you switch apps.

## Start menu settings

Show a start card with segmented buttons for each setting, remembered between visits:

- **Steering**: Drag on road, ◀ ▶ buttons
- **Drag sensitivity**: Low, Medium, High
- **Top speed**: Relaxed, Normal, Fast
- **Traffic**: Light, Normal, Heavy
- **Clock**: Relaxed, Normal, Tight
- **Mode**: Stages, Endless
- **Controls side**: Buttons right, Buttons left
- **Sound**: On, Off
- **Vibration**: On, Off

## Levels

10 levels that unlock in order, shown as a numbered grid with a lock icon on locked ones. The selected level's description appears under the grid:

1. Dune Dawn
2. Cactus Alley
3. Mesa Road
4. Salt Flats
5. Canyon Run
6. Rattler Pass
7. Dust Devil
8. Red Rock Rise
9. Mirage Mile
10. Sunset Summit

## Challenges

A collapsible checklist on the start card. When the player completes one, mark it done, save it, and show a short toast:

- Finish Mesa Road (stage 3)
- Finish Rattler Pass (stage 6)
- Finish Sunset Summit (stage 10)
- Pass 25 cars in one run
- Finish a stage without a crash
- Reach a checkpoint with 10+ seconds spare
- Drive 3 miles in Endless mode
- Hit top speed

## Look and feel

- Type: Russo One + Chakra Petch
- Palette: synthwave sunset: purple-to-orange sky, striped sun, desert sand, red-and-white rumble strips, orange accent (#ffb238)
- Layout: full-screen canvas, horizon 30% down
- A score/status strip at the top and a one-line control hint at the bottom. End-of-game and level-clear cards offer a clear next action (retry, next level, menu).
- Particles, small animations and screen feedback for hits, clears and wins. Keep motion purposeful.

## Technical requirements

- Render the playfield on a `<canvas>` at a fixed logical size, scaled to fit the available space with devicePixelRatio for sharpness. Clamp frame delta time (0 to 50 ms) so tab switches never break physics.
- Use pointer events for touch and mouse, with `touch-action: none` on the play area so the page never scrolls while playing.
- Respect safe-area insets (`env(safe-area-inset-*)`), keep at least a 16px side gutter, and never scroll horizontally at 360–400px widths.
- Save settings, unlocked levels, best scores and completed challenges in `localStorage`, wrapped in try/catch so the game still works when storage is blocked.
- No `alert()`/`confirm()`/`prompt()`; build any confirmation into the page.
- Test it: the game must load without console errors, start from the menu, and be playable start to finish.
