# Prompt: Bench Rounds

Paste the prompt below into Claude (or another capable coding model) to recreate this game as a single HTML file. Adjust anything you like before sending.

---

Build a complete, polished browser game called **Bench Rounds**, inspired by clinical lab trivia, as **one self-contained HTML file** (inline CSS and JavaScript, no frameworks or build step; Google Fonts is the only allowed external resource, always with a system-font fallback). Use original characters and artwork drawn in code. Do not copy any trademarked characters, names or logos.

## The game

Clinical laboratory trivia across the benches: hematology, chemistry, microbiology, blood bank, urinalysis, coag and specimen handling. Solo or pass-and-play for 2–4.

Menu text to show the player:

> Clinical lab trivia across seven benches. Read the question, then tap one of the four big answer buttons. Solo, or pass the phone around with 2 to 4 players.

## Controls (phone first)

Big full-width answer buttons. Each answer shows an explanation; tap Next to continue.

Touch must feel good on a phone held in portrait. Add matching keyboard controls for desktop.

## Rules and features

- Settings for categories, difficulty, question count and timer.
- A header mute button and pause button; the game pauses itself when you switch apps.

## Start menu settings

Show a start card with segmented buttons for each setting, remembered between visits:

- **Players**: Solo, 2, 3, 4
- **Difficulty**: Easy, Mixed, Hard, Ramp up
- **Questions each**: 5, 10, 15, 20
- **Clock per question**: Off, 15 s, 20 s, 30 s
- **Benches**: All seven, Pick…
- **Sound**: On, Off
- **Vibration**: On, Off

## Challenges

A collapsible checklist on the start card. When the player completes one, mark it done, save it, and show a short toast:

- Answer 5 in a row correctly
- Answer correctly within 3 seconds (clock on)
- Finish a solo round of 5+ questions with none wrong
- Get 5 Hard questions right in one round
- Get a question right on every bench
- Finish a game with 3 or 4 players
- Finish a 20-question round

## Look and feel

- Type: IBM Plex Sans / Condensed / Mono
- Palette: specimen-label cards; light and dark themes; category colors match tube caps (lavender, light blue, gold, green, pink, yellow, gray)
- Layout: HTML/CSS cards, no canvas
- A score/status strip at the top and a one-line control hint at the bottom. End-of-game and level-clear cards offer a clear next action (retry, next level, menu).
- Particles, small animations and screen feedback for hits, clears and wins. Keep motion purposeful.

## Technical requirements

- Build the interface with semantic HTML and CSS (cards, buttons, a responsive single column) and support light and dark themes. If you add animation, clamp frame delta time (0 to 50 ms) so tab switches never break physics.
- Use pointer events for touch and mouse, with `touch-action: none` on the play area so the page never scrolls while playing.
- Respect safe-area insets (`env(safe-area-inset-*)`), keep at least a 16px side gutter, and never scroll horizontally at 360–400px widths.
- Save settings, unlocked levels, best scores and completed challenges in `localStorage`, wrapped in try/catch so the game still works when storage is blocked.
- No `alert()`/`confirm()`/`prompt()`; build any confirmation into the page.
- Test it: the game must load without console errors, start from the menu, and be playable start to finish.
