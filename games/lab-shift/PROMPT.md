# Prompt: Lab Shift

Paste the prompt below into Claude (or another capable coding model) to recreate this game as a single HTML file. Adjust anything you like before sending.

---

Build a complete, polished browser game called **Lab Shift**, inspired by a hospital clinical-lab shift, as **one self-contained HTML file** (inline CSS and JavaScript, no frameworks or build step; Google Fonts is the only allowed external resource, always with a system-font fallback). Use original characters and artwork drawn in code. Do not copy any trademarked characters, names or logos.

## The game

Work a lab shift: route arriving specimens to the right department or reject them for the right reason, then release results, call critical values and rerun delta-check failures. Ten shifts, up to a mass-casualty night.

Menu text to show the player:

> You run receiving at a hospital lab. Tap a specimen row to inspect it, then use the six buttons under the board: send it to the right department, or reject it with the right reason. Later, release results, CALL critical values, and rerun delta-check failures. Fast and accurate wins.

## Controls (phone first)

Tap a specimen to inspect it, then tap one of the big action buttons under the board. A REF button opens tube-top, critical-value and rejection references.

Touch must feel good on a phone held in portrait. Add matching keyboard controls for desktop.

## Rules and features

- Critical values and rules follow common references; local lab policy can differ.
- A header mute button and pause button; the game pauses itself when you switch apps.

## Start menu settings

Show a start card with segmented buttons for each setting, remembered between visits:

- **Difficulty**: Trainee, Tech, Senior
- **Shift length**: Short 4h, Standard 8h, Long 12h
- **Hints**: Off, Show rules, Full guide
- **Department focus**: All, Chem, Heme, Coag, Micro, Blood Bank
- **Sound**: On, Off
- **Vibration**: On, Off

## Levels

10 levels that unlock in order, shown as a numbered grid with a lock icon on locked ones. The selected level's description appears under the grid:

1. Day 1: Orientation
2. Day: Morning Draw
3. Evening: Clinic Backlog
4. Night: Quiet Hours
5. Day: ER Surge
6. Evening: Transfusion Night
7. Night: ICU Rounds
8. Day: Outbreak Day
9. Night: Skeleton Crew
10. MASS CASUALTY

## Challenges

A collapsible checklist on the start card. When the player completes one, mark it done, save it, and show a short toast:

- Reject a hemolyzed specimen
- Catch a mislabeled tube
- Call a critical within 10 minutes of the result
- Rerun a delta-check failure
- Release a STAT within 15 minutes of arrival
- Finish a shift with no errors (8+ decisions)
- Pass the Mass Casualty shift

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
