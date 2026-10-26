# Prompt: Under the Scope

Paste the prompt below into Claude (or another capable coding model) to recreate this game as a single HTML file. Adjust anything you like before sending.

---

Build a complete, polished browser game called **Under the Scope**, inspired by microscope slide identification, as **one self-contained HTML file** (inline CSS and JavaScript, no frameworks or build step; Google Fonts is the only allowed external resource, always with a system-font fallback). Use original characters and artwork drawn in code. Do not copy any trademarked characters, names or logos.

## The game

Identify what you see in a drawn microscope field: 27 specimens across red-cell morphology, white cells, Gram and acid-fast stains, and urine sediment. Each look is a freshly randomized field with realistic stain backgrounds, platelets, debris and refractile crystals.

## Controls (phone first)

Tap the answer. Another view redraws the same specimen with a new random field.

Touch must feel good on a phone held in portrait. Add matching keyboard controls for desktop.

## Rules and features

- Difficulty: Student (slide type shown, 4 choices, no clock), Tech (slide type hidden, 25 s clock), Pathologist (6 choices from any bench, 15 s clock).
- Solo or pass-and-play for two; streak bonuses.
- Every answer explains the key identifying features.

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
