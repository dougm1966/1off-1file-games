# Prompt: Oche

Paste the prompt below into Claude (or another capable coding model) to recreate this game as a single HTML file. Adjust anything you like before sending.

---

Build a complete, polished browser game called **Oche**, inspired by pub darts, as **one self-contained HTML file** (inline CSS and JavaScript, no frameworks or build step; Google Fonts is the only allowed external resource, always with a system-font fallback). Use original characters and artwork drawn in code. Do not copy any trademarked characters, names or logos.

## The game

Darts with x01 (301/501, optional double-out), Cricket and Around the Clock. Your aim drifts like a real hand, so you time the release.

Menu text to show the player:

> Hold your finger on the board to aim. Your hand drifts, so watch the crosshair and let go at the right moment.

## Controls (phone first)

Hold a finger on the board to aim (the crosshair appears above your finger and drifts), release to throw. Three darts per turn.

Touch must feel good on a phone held in portrait. Add matching keyboard controls for desktop.

## Start menu settings

Show a start card with segmented buttons for each setting, remembered between visits:

- **Game**: x01, Cricket, Around the clock
- **Players**: Solo, Two players, Vs CPU
- **x01 start**: 301, 501
- **Double out**: On, Off
- **Hand**: Steady, Normal, Shaky
- **Around the clock: doubles/triples skip ahead**: Off, On

## Challenges

A collapsible checklist on the start card. When the player completes one, mark it done, save it, and show a short toast:

- Hit an inner bull
- Throw a 180
- Check out on a double
- Finish from 100 or more in one turn
- Win a game of Cricket
- Finish Around the Clock in 45 darts or fewer

## Look and feel

- Type: Alfa Slab One for display, system UI for body text
- Palette: background #14100c, text #f6efe2, accent #e2b04a
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
