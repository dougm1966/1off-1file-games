# Prompt: Rink Rivals

Paste the prompt below into Claude (or another capable coding model) to recreate this game as a single HTML file. Adjust anything you like before sending.

---

Build a complete, polished browser game called **Rink Rivals**, inspired by air hockey, as **one self-contained HTML file** (inline CSS and JavaScript, no frameworks or build step; Google Fonts is the only allowed external resource, always with a system-font fallback). Use original characters and artwork drawn in code. Do not copy any trademarked characters, names or logos.

## The game

Air hockey on one phone: two players each hold an end, or one player climbs a ten-opponent CPU ladder.

Menu text to show the player:

> Drag a finger on your half and your paddle follows just ahead of it. Hit the puck into the other goal. Two players: lay the phone flat, one at each end, and play at the same time. Solo: climb 10 CPU opponents.

## Controls (phone first)

Each half of the rink is tinted in its player's colour and labelled. A finger belongs to the half where it first touched and keeps controlling that paddle until it lifts, even if it crosses the centre line, so two players never interfere. The paddle sits a little ahead of your finger so you can see it.

Touch must feel good on a phone held in portrait. Add matching keyboard controls for desktop.

## Rules and features

- Settings for mode, score to win and puck speed; 7 challenges.
- A header mute button and pause button; the game pauses itself when you switch apps.

## Start menu settings

Show a start card with segmented buttons for each setting, remembered between visits:

- **Mode**: Vs CPU ladder, Two players
- **First to**: 5, 7, 11
- **Puck**: Chill, Normal, Fast
- **Paddle size**: Normal, Big
- **Sound**: On, Off
- **Vibration**: On, Off

## Levels

10 levels that unlock in order, shown as a numbered grid with a lock icon on locked ones. The selected level's description appears under the grid:

1. Rookie
2. Junior
3. Club
4. Varsity
5. Semi-pro
6. Pro
7. All-star
8. Veteran
9. Champion
10. Legend

## Challenges

A collapsible checklist on the start card. When the player completes one, mark it done, save it, and show a short toast:

- Win against the CPU without letting one in
- Win after being down by 3
- Score within 3.5 seconds of a faceoff
- Score with a top-speed shot
- Beat the Semi-pro (level 5)
- Beat the Legend (level 10)
- Finish a two-player match

## Look and feel

- Type: Saira Condensed for display, system UI for body text
- Palette: background #0b1220, text #eef5ff, accent #36d1ff
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
