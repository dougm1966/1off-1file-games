# Prompt: Swarm Wing

Paste the prompt below into Claude (or another capable coding model) to recreate this game as a single HTML file. Adjust anything you like before sending.

---

Build a complete, polished browser game called **Swarm Wing**, inspired by Galaga, as **one self-contained HTML file** (inline CSS and JavaScript, no frameworks or build step; Google Fonts is the only allowed external resource, always with a system-font fallback). Use original characters and artwork drawn in code. Do not copy any trademarked characters, names or logos.

## The game

Shoot down swooping waves of insect-like ships over 10 stages, including no-return-fire challenge stages. Catch a wingman capsule for a twin ship; a hit costs the wingman before it costs a life.

Menu text to show the player:

> The swarm loops in, forms up, then peels off to dive at you. Hold ◀ ▶ to move and the big FIRE button to shoot, at the same time. Diving hits score double. Catch the cyan capsule for a wingman.

## Controls (phone first)

◀ ▶ hold buttons and a FIRE button, usable together. Auto-fire and a 'Drag ship' mode are settings.

Touch must feel good on a phone held in portrait. Add matching keyboard controls for desktop.

## Rules and features

- 10 stages that unlock, and 7 challenges.
- A header mute button and pause button; the game pauses itself when you switch apps.

## Start menu settings

Show a start card with segmented buttons for each setting, remembered between visits:

- **Difficulty**: Easy, Normal, Hard
- **Controls**: ◀ ▶ + FIRE, Drag ship
- **Auto-fire (buttons mode)**: Off, On
- **Lives**: 3, 5
- **Challenge stages**: On, Off
- **Controls side**: Buttons right, Buttons left
- **Sound**: On, Off
- **Vibration**: On, Off

## Levels

10 levels that unlock in order, shown as a numbered grid with a lock icon on locked ones. The selected level's description appears under the grid:

1. Warm-up
2. Swoop
3. Pincer
4. Challenge I
5. Dive Bombers
6. Crossfire
7. Leaders' Guard
8. Challenge II
9. Storm
10. Final Swarm

## Challenges

A collapsible checklist on the start card. When the player completes one, mark it done, save it, and show a short toast:

- Clear stage 1
- Catch a wingman capsule
- Shoot 8 diving enemies in one stage
- Clear a stage without losing a ship
- Hit 30 of 40 in a challenge stage
- Perfect a challenge stage (40 of 40)
- Clear the Final Swarm (stage 10)

## Look and feel

- Type: Exo 2 for display, system UI for body text
- Palette: background #06040f, text #f1ecff, accent #ffd23f
- Layout: logical canvas 360×620, scaled to fit the screen
- A score/status strip at the top and a one-line control hint at the bottom. End-of-game and level-clear cards offer a clear next action (retry, next level, menu).
- Particles, small animations and screen feedback for hits, clears and wins. Keep motion purposeful.

## Technical requirements

- Render the playfield on a `<canvas>` at a fixed logical size, scaled to fit the available space with devicePixelRatio for sharpness. Clamp frame delta time (0 to 50 ms) so tab switches never break physics.
- Use pointer events for touch and mouse, with `touch-action: none` on the play area so the page never scrolls while playing.
- Respect safe-area insets (`env(safe-area-inset-*)`), keep at least a 16px side gutter, and never scroll horizontally at 360–400px widths.
- Save settings, unlocked levels, best scores and completed challenges in `localStorage`, wrapped in try/catch so the game still works when storage is blocked.
- No `alert()`/`confirm()`/`prompt()`; build any confirmation into the page.
- Test it: the game must load without console errors, start from the menu, and be playable start to finish.
