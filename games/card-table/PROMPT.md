# Prompt: Card Table

Paste the prompt below into Claude (or another capable coding model) to recreate this game as a single HTML file. Adjust anything you like before sending.

---

Build a complete, polished browser game called **Card Table**, inspired by Hearts, Spades and Euchre, as **one self-contained HTML file** (inline CSS and JavaScript, no frameworks or build step; Google Fonts is the only allowed external resource, always with a system-font fallback). Use original characters and artwork drawn in code. Do not copy any trademarked characters, names or logos.

## The game

Three classic trick-taking card games against three CPU players, with Spades and Euchre played in partnerships.

Menu text to show the player:

> Hearts, Spades or Euchre against three CPU players. Your cards fan along the bottom: tap one to raise it, tap it again (or press PLAY) to play it. Dimmed cards can't be played right now.
> Targets (short / normal / long): Hearts 50 / 100 / 150 · Spades 200 / 300 / 500 · Euchre 5 / 10 / 15.

## Controls (phone first)

Tap a card to raise it, tap it again to play. ◀ ▶ and PLAY buttons select precisely when the hand is crowded. Cards you can't legally play are dimmed.

Touch must feel good on a phone held in portrait. Add matching keyboard controls for desktop.

## Rules and features

- Settings for the game, target score, CPU skill and house rules (passing, blind nil, stick the dealer).
- A header mute button and pause button; the game pauses itself when you switch apps.

## Start menu settings

Show a start card with segmented buttons for each setting, remembered between visits:

- **Game**: Hearts, Spades, Euchre
- **Target score**: Short, Normal, Long
- **CPU skill**: Easy, Normal, Hard
- **Card back**: Blue, Red, Green, Gold
- **Speed**: Slow, Normal, Fast
- **Hearts: Jack of Diamonds −10**: Off, On
- **Euchre: stick the dealer**: On, Off
- **Controls side**: Buttons right, Buttons left
- **Sound**: On, Off
- **Vibration**: On, Off

## Challenges

A collapsible checklist on the start card. When the player completes one, mark it done, save it, and show a short toast:

- Win a game of Hearts
- Shoot the moon in Hearts
- Win a game of Spades
- Make a nil bid in Spades
- Win a game of Euchre
- Euchre the other team (they make it, take under 3)
- Go alone and take 3+ tricks in Euchre

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
