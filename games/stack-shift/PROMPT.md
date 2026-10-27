# Prompt: Stack Shift

Paste the prompt below into Claude (or another capable coding model) to recreate this game as a single HTML file. Adjust anything you like before sending.

---

Build a complete, polished browser game called **Stack Shift**, inspired by Tetris-style falling blocks, as **one self-contained HTML file** (inline CSS and JavaScript, no frameworks or build step; Google Fonts is the only allowed external resource, always with a system-font fallback). Use original characters and artwork drawn in code. Do not copy any trademarked characters, names or logos.

## The game

Falling-block stacking with a seven-piece bag, ghost piece, hold and three-piece preview. Marathon, 40-line Sprint and 2-minute Ultra modes.

Menu text to show the player:

> Slide falling blocks into full rows to clear them. Use ◀ ▶ and ▼ on one side, and ROTATE, DROP and HOLD on the other. Hold ◀ or ▶ to keep sliding. Pick a start level; reach higher levels in Marathon to unlock more.

## Controls (phone first)

Buttons under the board: ◀ ▶ (hold to slide) and ▼ soft drop on the left; ROTATE, DROP and HOLD on the right. Board gestures (drag, tap to rotate, swipe down to drop) are an optional extra.

Touch must feel good on a phone held in portrait. Add matching keyboard controls for desktop.

## Rules and features

- 10 start levels that unlock, and 7 challenges.
- A header mute button and pause button; the game pauses itself when you switch apps.

## Start menu settings

Show a start card with segmented buttons for each setting, remembered between visits:

- **Mode**: Marathon, 40-line sprint, Ultra 2:00
- **Ghost piece**: On, Off
- **Hold-to-repeat speed**: Quick, Normal, Relaxed
- **Board gestures too**: Off, On
- **Controls side**: Buttons right, Buttons left
- **Sound**: On, Off
- **Vibration**: On, Off

## Levels

10 levels that unlock in order, shown as a numbered grid with a lock icon on locked ones. The selected level's description appears under the grid:

1. Level 1
2. Level 2
3. Level 3
4. Level 4
5. Level 5
6. Level 6
7. Level 7
8. Level 8
9. Level 9
10. Level 10

## Challenges

A collapsible checklist on the start card. When the player completes one, mark it done, save it, and show a short toast:

- Reach level 5
- Clear 4 rows at once
- Land a T-spin
- Chain 4 clears in a row
- Two Tetris/T-spin clears back to back
- Finish a 40-line sprint
- Score 3000 in Ultra

## Look and feel

- Type: Bungee + Space Mono
- Palette: navy (#121a33) with yellow accent (#ffcf3f); bevelled blocks in the classic seven colors
- Layout: board canvas plus side rail for hold/next/score
- A score/status strip at the top and a one-line control hint at the bottom. End-of-game and level-clear cards offer a clear next action (retry, next level, menu).
- Particles, small animations and screen feedback for hits, clears and wins. Keep motion purposeful.

## Technical requirements

- Render the playfield on a `<canvas>` at a fixed logical size, scaled to fit the available space with devicePixelRatio for sharpness. Clamp frame delta time (0 to 50 ms) so tab switches never break physics.
- Use pointer events for touch and mouse, with `touch-action: none` on the play area so the page never scrolls while playing.
- Respect safe-area insets (`env(safe-area-inset-*)`), keep at least a 16px side gutter, and never scroll horizontally at 360–400px widths.
- Save settings, unlocked levels, best scores and completed challenges in `localStorage`, wrapped in try/catch so the game still works when storage is blocked.
- No `alert()`/`confirm()`/`prompt()`; build any confirmation into the page.
- Test it: the game must load without console errors, start from the menu, and be playable start to finish.
