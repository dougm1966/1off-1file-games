# Prompt: Pocket Puzzle Duel

Paste the prompt below into Claude (or another capable coding model) to recreate this game as a single HTML file. Adjust anything you like before sending.

---

Build a complete, polished browser game called **Pocket Puzzle Duel**, inspired by pool trick-shot puzzles, as **one self-contained HTML file** (inline CSS and JavaScript, no frameworks or build step; Google Fonts is the only allowed external resource, always with a system-font fallback). Use original characters and artwork drawn in code. Do not copy any trademarked characters, names or logos.

## The game

Two players take turns on the same pool trick-shot layout across 10 holes; clear the balls in the fewest strokes, golf style.

Menu text to show the player:

> Clear the table in the fewest strokes. Slide a finger on the table to turn your aim (it never jumps to your finger), set POWER, press SHOOT. Duel: two players pass the phone. Solo: beat par on 10 puzzles (clear one to unlock the next).

## Controls (phone first)

Slide a finger anywhere on the table to rotate the cue; it never snaps to your finger. Nudge buttons fine-tune the angle, a slider sets power, and SHOOT is lit whenever a shot is allowed. A guide line shows the first contact and a short deflection hint.

Touch must feel good on a phone held in portrait. Add matching keyboard controls for desktop.

## Rules and features

- A 'Pass to Player 2' card between turns.
- A header mute button and pause button; the game pauses itself when you switch apps.

## Start menu settings

Show a start card with segmented buttons for each setting, remembered between visits:

- **Mode**: Duel · 2 players, Solo puzzles
- **Duel length (holes)**: 3, 6, 10
- **Aim help**: Line only, Medium, Extra
- **Aim slide speed**: Fine, Normal, Quick
- **Table cloth**: Blue, Green, Red
- **Sound**: On, Off
- **Vibration**: On, Off

## Levels

10 levels that unlock in order, shown as a numbered grid with a lock icon on locked ones. The selected level's description appears under the grid:

1. Opening Shot
2. Three Ball
3. Rail Huggers
4. Bumpers
5. The Rack
6. Through the Gate
7. Bank Street
8. Plus Sign
9. Picket Fence
10. Grand Finale

## Challenges

A collapsible checklist on the start card. When the player completes one, mark it done, save it, and show a short toast:

- Clear a table at par or better
- Clear a table under par
- Pocket two balls with one shot
- Pocket a ball after it bounced off a rail
- Clear a table without a scratch
- Finish a two-player duel
- Clear Grand Finale (puzzle 10)

## Look and feel

- Type: Bungee (display) + Barlow / Barlow Condensed
- Palette: dark blue-green pool hall (#0d1317), tournament-blue cloth, walnut rails, brass accent (#d9a845)
- Layout: portrait canvas table 452×812
- A score/status strip at the top and a one-line control hint at the bottom. End-of-game and level-clear cards offer a clear next action (retry, next level, menu).
- Particles, small animations and screen feedback for hits, clears and wins. Keep motion purposeful.

## Technical requirements

- Render the playfield on a `<canvas>` at a fixed logical size, scaled to fit the available space with devicePixelRatio for sharpness. Clamp frame delta time (0 to 50 ms) so tab switches never break physics.
- Use pointer events for touch and mouse, with `touch-action: none` on the play area so the page never scrolls while playing.
- Respect safe-area insets (`env(safe-area-inset-*)`), keep at least a 16px side gutter, and never scroll horizontally at 360–400px widths.
- Save settings, unlocked levels, best scores and completed challenges in `localStorage`, wrapped in try/catch so the game still works when storage is blocked.
- No `alert()`/`confirm()`/`prompt()`; build any confirmation into the page.
- Test it: the game must load without console errors, start from the menu, and be playable start to finish.
