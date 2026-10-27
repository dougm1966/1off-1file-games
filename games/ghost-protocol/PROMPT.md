# Prompt: Ghost Protocol

Paste the prompt below into Claude (or another capable coding model) to recreate this game as a single HTML file. Adjust anything you like before sending.

---

Build a complete, polished browser game called **Ghost Protocol**, inspired by top-down stealth games, as **one self-contained HTML file** (inline CSS and JavaScript, no frameworks or build step; Google Fonts is the only allowed external resource, always with a system-font fallback). Use original characters and artwork drawn in code. Do not copy any trademarked characters, names or logos.

## The game

Sneak through 10 guarded facilities past patrols with visible vision cones, cameras, locked doors and keycards. Rated on time, staying unseen and avoiding takedowns.

Menu text to show the player:

> Slip past the guards, download the intel, and reach the exit. Push the stick lightly (inside the dashed ring) to sneak silently; push past the ring to run, which makes noise. TAKEDOWN works only from behind. HIDE/USE hides in lockers and hacks terminals (hold). Stars 0/30.

## Controls (phone first)

A thumb stick moves you: a light push sneaks silently, a full push runs and makes a visible noise ring. TAKEDOWN and HIDE/USE buttons on the right.

Touch must feel good on a phone held in portrait. Add matching keyboard controls for desktop.

## Rules and features

- Guard alertness, vision-cone visibility and sneak assist settings; 7 challenges.
- A header mute button and pause button; the game pauses itself when you switch apps.

## Start menu settings

Show a start card with segmented buttons for each setting, remembered between visits:

- **Guard alertness**: Relaxed, Normal, Sharp
- **Vision cones**: Bright, Soft, Outline
- **Sneak assist**: Off, Near guards, Always sneak
- **Takedown aim assist**: On, Off
- **Noise ring when running**: On, Off
- **Controls side**: Buttons right, Buttons left
- **Sound**: On, Off
- **Vibration**: On, Off

## Levels

10 levels that unlock in order, shown as a numbered grid with a lock icon on locked ones. The selected level's description appears under the grid:

1. First Night
2. Loading Dock
3. Server Farm
4. Atrium
5. Cell Block
6. Control Room
7. Shelf Maze
8. The Vault
9. Rooftop
10. Ghost Protocol

## Challenges

A collapsible checklist on the start card. When the player completes one, mark it done, save it, and show a short toast:

- Clear a level without ever being spotted
- Clear a level under its par time
- Take down 3 guards in one level
- Hide and shake off a guard who was chasing you
- Blind the cameras at a switch
- Clear a level without ever running
- Clear Ghost Protocol (level 10)

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
