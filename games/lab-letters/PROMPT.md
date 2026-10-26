# Prompt: Lab Letters

Paste the prompt below into Claude (or another capable coding model) to recreate this game as a single HTML file. Adjust anything you like before sending.

---

Build a complete, polished browser game called **Lab Letters**, inspired by Wordle, as **one self-contained HTML file** (inline CSS and JavaScript, no frameworks or build step; Google Fonts is the only allowed external resource, always with a system-font fallback). Use original characters and artwork drawn in code. Do not copy any trademarked characters, names or logos.

## The game

Guess the five-letter lab word in six tries. Tiles show which letters are in the right spot or in the word.

Menu text to show the player:

> Guess the hidden five-letter word. Green means right letter, right spot. Gold means right letter, wrong spot. The lab list is all bench and body words. In Partner mode, one of you sets a word for the other.

## Controls (phone first)

Type with the on-screen keyboard (or a physical keyboard) and press Enter.

Touch must feel good on a phone held in portrait. Add matching keyboard controls for desktop.

## Start menu settings

Show a start card with segmented buttons for each setting, remembered between visits:

- **Words**: Lab & body words, Partner sets the word
- **Guesses**: 6, 8 · easier
- **Hard mode**: Off, Must reuse hints

## Challenges

A collapsible checklist on the start card. When the player completes one, mark it done, save it, and show a short toast:

- Solve a word
- Solve in 2 guesses
- Solve 5 in a row
- Solve in hard mode
- Solve a word your partner set
- Solve 10 words total

## Look and feel

- Type: Roboto Slab for display, system UI for body text
- Palette: background #121417, text #f2f4f7, accent #5fb27a
- Layout: logical canvas 360×600, scaled to fit the screen
- A score/status strip at the top and a one-line control hint at the bottom. End-of-game and level-clear cards offer a clear next action (retry, next level, menu).
- Particles, small animations and screen feedback for hits, clears and wins. Keep motion purposeful.

## Technical requirements

- Render the playfield on a `<canvas>` at a fixed logical size, scaled to fit the available space with devicePixelRatio for sharpness. Clamp frame delta time (0 to 50 ms) so tab switches never break physics.
- Use pointer events for touch and mouse, with `touch-action: none` on the play area so the page never scrolls while playing.
- Respect safe-area insets (`env(safe-area-inset-*)`), keep at least a 16px side gutter, and never scroll horizontally at 360–400px widths.
- Save settings, unlocked levels, best scores and completed challenges in `localStorage`, wrapped in try/catch so the game still works when storage is blocked.
- No `alert()`/`confirm()`/`prompt()`; build any confirmation into the page.
- Test it: the game must load without console errors, start from the menu, and be playable start to finish.
