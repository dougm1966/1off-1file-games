# Prompt: Stack Shift

Paste the prompt below into Claude (or another capable coding model) to recreate this game as a single HTML file. Adjust anything you like before sending.

---

Build a complete, polished browser game called **Stack Shift**, inspired by Tetris-style falling blocks, as **one self-contained HTML file** (inline CSS and JavaScript, no frameworks or build step; Google Fonts is the only allowed external resource, always with a system-font fallback). Use original characters and artwork drawn in code. Do not copy any trademarked characters, names or logos.

## The game

Classic falling-block stacking with seven-piece bag randomizer, ghost piece, hold slot and a three-piece next queue. Clear lines to score and level up.

## Controls (phone first)

On the board: drag sideways to move, tap to rotate, swipe down fast to hard-drop, drag down slowly to soft-drop. A button row offers left, right, rotate, soft drop, hard drop and hold.

Touch must feel good on a phone held in portrait. Add matching keyboard controls for desktop.

## Rules and features

- Speed increases every 10 lines; 1/2/3/4-line clears score 100/300/500/800 × level.
- Pause button and saved best score.

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
