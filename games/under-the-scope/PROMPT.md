# Prompt: Under the Scope

Paste the prompt below into Claude (or another capable coding model) to recreate this game as a single HTML file. Adjust anything you like before sending.

---

Build a complete, polished browser game called **Under the Scope**, inspired by microscope identification, as **one self-contained HTML file** (inline CSS and JavaScript, no frameworks or build step; Google Fonts is the only allowed external resource, always with a system-font fallback). Use original characters and artwork drawn in code. Do not copy any trademarked characters, names or logos.

## The game

Identify what you see in realistic microscope fields: blood smears, Gram and acid-fast stains, and urine sediment, at student, tech or pathologist level.

Menu text to show the player:

> Name what is under the microscope: blood smears, Gram and acid-fast stains, urine sediment. Tap ZOOM for 2× and drag to pan, then tap one of the answers. Every answer explains the key features.

## Controls (phone first)

Answer buttons under the eyepiece. A Zoom button switches between 1× and 2×; when zoomed, drag one finger to pan.

Touch must feel good on a phone held in portrait. Add matching keyboard controls for desktop.

## Rules and features

- Solo or pass-and-play for 2–4; settings for specimen types, level, number of fields and clock.
- A header mute button and pause button; the game pauses itself when you switch apps.

## Start menu settings

Show a start card with segmented buttons for each setting, remembered between visits:

- **Players**: Solo, 2, 3, 4
- **Specimens**: All, Blood, Stains, Urine
- **Level**: Student, Tech, Path
- **Fields each**: 5, 10, 15, 20
- **Clock**: By level, Off, 15 s, 30 s, 60 s
- **Sound**: On, Off
- **Vibration**: On, Off

## Challenges

A collapsible checklist on the start card. When the player completes one, mark it done, save it, and show a short toast:

- Identify 5 fields in a row
- Finish a solo round of 5+ fields with none wrong
- Get 5 right in one round after zooming in on each
- Identify 5 urine sediment fields in one round
- Get 5 right at Pathologist level in one round
- Finish a round with 3 or 4 players

## Look and feel

- Type: IBM Plex Sans / Condensed / Mono
- Palette: dark UI (#0e1114) around a circular eyepiece with vignette and grain; Wright-stain pinks/purples, Gram stain pinks/purples, blue AFB counterstain, beige unstained urine
- Layout: canvas 760×760 eyepiece
- A score/status strip at the top and a one-line control hint at the bottom. End-of-game and level-clear cards offer a clear next action (retry, next level, menu).
- Particles, small animations and screen feedback for hits, clears and wins. Keep motion purposeful.

## Technical requirements

- Render the playfield on a `<canvas>` at a fixed logical size, scaled to fit the available space with devicePixelRatio for sharpness. Clamp frame delta time (0 to 50 ms) so tab switches never break physics.
- Use pointer events for touch and mouse, with `touch-action: none` on the play area so the page never scrolls while playing.
- Respect safe-area insets (`env(safe-area-inset-*)`), keep at least a 16px side gutter, and never scroll horizontally at 360–400px widths.
- Save settings, unlocked levels, best scores and completed challenges in `localStorage`, wrapped in try/catch so the game still works when storage is blocked.
- No `alert()`/`confirm()`/`prompt()`; build any confirmation into the page.
- Test it: the game must load without console errors, start from the menu, and be playable start to finish.
