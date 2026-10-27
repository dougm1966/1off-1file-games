# Prompt: Immune Response

Paste the prompt below into Claude (or another capable coding model) to recreate this game as a single HTML file. Adjust anything you like before sending.

---

Build a complete, polished browser game called **Immune Response**, inspired by tower defense, as **one self-contained HTML file** (inline CSS and JavaScript, no frameworks or build step; Google Fonts is the only allowed external resource, always with a system-font fallback). Use original characters and artwork drawn in code. Do not copy any trademarked characters, names or logos.

## The game

Defend an organ from waves of bacteria, viruses and fungi by placing immune cells along the vessel: neutrophils, macrophages, NK cells, B cells and T helpers. Ten levels with different vessel layouts.

Menu text to show the player:

> Germs travel along the blood vessel to the organ. Tap a glowing spot to build an immune cell, tap a cell to upgrade or sell it, and press NEXT WAVE when ready. Stars 0/30.

## Controls (phone first)

Tap an empty build spot to open a card of cells with their costs; tap a placed cell to upgrade, sell or change its target. Speed, Fever and Next wave buttons sit under the board.

Touch must feel good on a phone held in portrait. Add matching keyboard controls for desktop.

## Rules and features

- Three difficulties and 7 challenges.
- A header mute button and pause button; the game pauses itself when you switch apps.

## Start menu settings

Show a start card with segmented buttons for each setting, remembered between visits:

- **Difficulty**: Easy, Normal, Hard
- **Mode**: Campaign, Endless
- **Auto-send next wave**: Off, On
- **Start speed**: 1×, 2×
- **New cells target**: First, Strong, Weak, Last
- **Range circles**: Selected, All, Off
- **Health bars**: On, Off
- **Damage numbers**: On, Off
- **Controls side**: Buttons right, Buttons left
- **Sound**: On, Off
- **Vibration**: On, Off

## Levels

10 levels that unlock in order, shown as a numbered grid with a lock icon on locked ones. The selected level's description appears under the grid:

1. Paper Cut
2. Sore Throat
3. Gut Instinct
4. Flu Season
5. Kidney Stand
6. Thrush
7. Lung Siege
8. Liver Gate
9. Brain Barrier
10. Sepsis Storm

## Challenges

A collapsible checklist on the start card. When the player completes one, mark it done, save it, and show a short toast:

- Neutrophil - first responder; fast, cheap, great vs bacteria.
- Macrophage - big eater; engulfs groups of bacteria and fungi.
- NK cell - kills infected cells; best vs viruses.
- B cell - antibodies tag germs (blue Y), slowing them and making them take more damage.
- T helper - releases cytokines that speed up and strengthen nearby cells.
- Fever - slows every germ for 8 seconds.
- Armour (TB, MRSA, mold) - big hits work best.
- Splitters (Strep, Candida) - break into smaller germs when killed.
- Tap a germ to learn about it.
- Clear a level without losing organ health
- Clear a level using only innate cells (no B or T cells)
- Have one T helper boosting 3 cells at once
- Kill 40 antibody-marked germs in one game
- Trigger a Fever while 10+ germs are on screen
- Clear level 5 on Hard
- Clear Sepsis Storm (level 10)

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
