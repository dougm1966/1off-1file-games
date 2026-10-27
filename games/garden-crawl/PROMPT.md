# Prompt: Garden Crawl

Paste the prompt below into Claude (or another capable coding model) to recreate this game as a single HTML file. Adjust anything you like before sending.

---

Build a complete, polished browser game called **Garden Crawl**, inspired by Centipede, as **one self-contained HTML file** (inline CSS and JavaScript, no frameworks or build step; Google Fonts is the only allowed external resource, always with a system-font fallback). Use original characters and artwork drawn in code. Do not copy any trademarked characters, names or logos.

## The game

A garden gnome holds off a centipede winding down through mushrooms, plus spiders and scouts, over 10 waves. Shot segments split the centipede in two.

Menu text to show the player:

> A centipede winds down through your mushroom patch. Put a finger anywhere on the board and drag: the gnome slides the same way inside the outlined zone, and sprays while your finger is down. Each hit segment sprouts a mushroom and splits the train.

## Controls (phone first)

Drag anywhere on the board: the gnome moves by however far your finger moves, inside its outlined zone, and fires automatically while a finger is down. A setting gives a thumb stick plus FIRE button instead.

Touch must feel good on a phone held in portrait. Add matching keyboard controls for desktop.

## Rules and features

- 10 waves that unlock, and 7 challenges.
- A header mute button and pause button; the game pauses itself when you switch apps.

## Start menu settings

Show a start card with segmented buttons for each setting, remembered between visits:

- **Controls**: Drag on board, Stick + Fire
- **Difficulty**: Easy, Normal, Hard
- **Gnomes**: 3, 5
- **Drag speed**: Slow, Normal, Fast
- **Controls side**: Buttons right, Buttons left
- **Sound**: On, Off
- **Vibration**: On, Off

## Levels

10 levels that unlock in order, shown as a numbered grid with a lock icon on locked ones. The selected level's description appears under the grid:

1. Dewy Dawn
2. Clover Patch
3. Slug Trail
4. Spider Web
5. Toadstool Ring
6. Bramble Row
7. Midnight Mulch
8. Thorn Hedge
9. Mushroom Maze
10. The Great Crawl

## Challenges

A collapsible checklist on the start card. When the player completes one, mark it done, save it, and show a short toast:

- Shoot a centipede head
- Split the centipede into 3 pieces
- Shoot a spider up close (900 points)
- Destroy 20 mushrooms in one game
- Clear a wave without losing a gnome
- Clear Toadstool Ring (wave 5)
- Clear The Great Crawl

## Look and feel

- Type: Fredoka for display, system UI for body text
- Palette: background #120d1f, text #f6f0ff, accent #9cff57
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
