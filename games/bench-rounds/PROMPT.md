# Prompt: Bench Rounds

Paste the prompt below into Claude (or another capable coding model) to recreate this game as a single HTML file. Adjust anything you like before sending.

---

Build a complete, polished browser game called **Bench Rounds**, inspired by clinical lab trivia, as **one self-contained HTML file** (inline CSS and JavaScript, no frameworks or build step; Google Fonts is the only allowed external resource, always with a system-font fallback). Use original characters and artwork drawn in code. Do not copy any trademarked characters, names or logos.

## The game

Multiple-choice trivia for a hospital lab tech: 65 questions across hematology, coagulation, chemistry, microbiology, blood bank, urinalysis and QC. Every answer comes with a short explanation.

## Controls (phone first)

Tap an answer. In two-player mode, pass the phone when the hand-off screen appears.

Touch must feel good on a phone held in portrait. Add matching keyboard controls for desktop.

## Rules and features

- Solo or two players taking turns, each with their own questions.
- Pick which benches to include and how many questions each.
- Optional 20-second clock; streaks earn bonus points.
- Category colors match tube-cap colors.

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
