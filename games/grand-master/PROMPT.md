# Prompt: Grand Master

Paste the prompt below into Claude (or another capable coding model) to recreate this game as a single HTML file. Adjust anything you like before sending.

---

Build a complete, polished browser game called **Grand Master**, inspired by chess, as **one self-contained HTML file** (inline CSS and JavaScript, no frameworks or build step; Google Fonts is the only allowed external resource, always with a system-font fallback). Use original characters and artwork drawn in code. Do not copy any trademarked characters, names or logos.

## The game

Full chess against a CPU with five strengths, or pass-and-play: castling, en passant, promotion, and every draw rule.

Menu text to show the player:

> Classic chess. Tap a piece, then tap a dot to move it, or drag a piece: it floats above your finger so you can see where it lands. Buttons under the board: undo, hint, flip and move list.

## Controls (phone first)

Tap a piece to see its legal moves, then tap a square; or drag the piece, which is drawn above your finger. Undo, hint and resign buttons.

Touch must feel good on a phone held in portrait. Add matching keyboard controls for desktop.

## Rules and features

- Optional clock, legal-move dots, last-move highlight and a pass card for two players.
- A header mute button and pause button; the game pauses itself when you switch apps.

## Start menu settings

Show a start card with segmented buttons for each setting, remembered between visits:

- **Opponent**: CPU, Pass & play
- **CPU strength**: 1, 2, 3, 4, 5
- **You play**: White, Black, Random
- **Board**: Walnut, Slate, Forest, Rose
- **Show legal moves**: On, Off
- **Clock (per side)**: None, 5 min, 10 min
- **Rotate board for Player 2**: Off, On
- **“Pass the phone” card**: On, Off
- **Sound**: On, Off
- **Vibration**: On, Off

## Challenges

A collapsible checklist on the start card. When the player completes one, mark it done, save it, and show a short toast:

- Beat the CPU
- Beat Club strength (3) or higher
- Beat Strong strength (4) or higher
- Checkmate the CPU in 30 moves or fewer
- Win without using Undo or Hint
- Castle
- Capture en passant
- Promote a pawn

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
