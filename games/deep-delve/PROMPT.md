# Prompt: Deep Delve

Paste the prompt below into Claude (or another capable coding model) to recreate this game as a single HTML file. Adjust anything you like before sending.

---

Build a complete, polished browser game called **Deep Delve**, inspired by roguelike dungeon crawlers, as **one self-contained HTML file** (inline CSS and JavaScript, no frameworks or build step; Google Fonts is the only allowed external resource, always with a system-font fallback). Use original characters and artwork drawn in code. Do not copy any trademarked characters, names or logos.

## The game

A turn-based dungeon crawl through 10 generated floors with fog of war, monsters, items and permadeath. Daily dungeon mode gives everyone the same layout that day.

Menu text to show the player:

> Delve ten floors, find the stairs on each and defeat the Hollow King. Use the D-pad to move and attack, or tap a floor tile to walk there. Death is permanent.
> Daily dungeon today: seed 20261027. Best floor 0.

## Controls (phone first)

A D-pad moves and attacks one square per press (hold to repeat). Tap a visible floor tile to walk there. WAIT, USE and STAIRS buttons.

Touch must feel good on a phone held in portrait. Add matching keyboard controls for desktop.

## Rules and features

- Three classes and three difficulties.
- A header mute button and pause button; the game pauses itself when you switch apps.

## Start menu settings

Show a start card with segmented buttons for each setting, remembered between visits:

- **Class**: Warrior, Rogue, Mage
- **Difficulty**: Easy, Normal, Hard
- **Dungeon**: Random, Daily
- **Auto-pickup**: On, Off
- **Tap floor to travel**: On, Off
- **Controls side**: Buttons right, Buttons left
- **Sound**: On, Off
- **Vibration**: On, Off

## Levels

10 levels that unlock in order, shown as a numbered grid with a lock icon on locked ones. The selected level's description appears under the grid:

1. The Cellars
2. Rat Warrens
3. Mossy Halls
4. Bone Gallery
5. Slime Pits
6. The Barracks
7. Cursed Library
8. Ogre Den
9. Shadow Vault
10. The Hollow Throne

## Challenges

A collapsible checklist on the start card. When the player completes one, mark it done, save it, and show a short toast:

- Reach floor 3
- Reach floor 5
- Slay 25 enemies in one run
- Collect 250 gold in one run
- Reach character level 8
- Reach floor 3 in the Daily dungeon
- Defeat the Hollow King

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
