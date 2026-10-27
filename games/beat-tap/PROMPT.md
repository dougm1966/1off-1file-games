# Prompt: Beat Tap

Paste the prompt below into Claude (or another capable coding model) to recreate this game as a single HTML file. Adjust anything you like before sending.

---

Build a complete, polished browser game called **Beat Tap**, inspired by rhythm games, as **one self-contained HTML file** (inline CSS and JavaScript, no frameworks or build step; Google Fonts is the only allowed external resource, always with a system-font fallback). Use original characters and artwork drawn in code. Do not copy any trademarked characters, names or logos.

## The game

Tap along to 10 original synthesized songs as notes fall down the lanes: single notes, chords and holds, judged Perfect, Great, Good or Miss.

Menu text to show the player:

> Tap the lit pad under a lane when its note reaches the line. Use several fingers for chords and keep a finger down on long notes. If notes feel early or late, run the timing calibration.

## Controls (phone first)

Four big labelled tap pads under the lanes, one finger per lane; chords use several fingers at once and hold notes stay down. Keys D F J K also work. A calibration screen lines up audio and visuals.

Touch must feel good on a phone held in portrait. Add matching keyboard controls for desktop.

## Rules and features

- Three difficulties, note speed, 3 or 4 lanes, timing windows and a no-fail practice mode with slower tempos.
- A header mute button and pause button; the game pauses itself when you switch apps.

## Start menu settings

Show a start card with segmented buttons for each setting, remembered between visits:

- **Difficulty**: Easy, Normal, Hard
- **Note speed**: Slow, Medium, Fast, Turbo
- **Lanes**: 3 lanes, 4 lanes
- **Timing windows**: Lenient, Standard, Strict
- **Practice (no fail, nothing saved)**: Off, On
- **Practice tempo**: 100%, 75%, 50%
- **Tap sound**: On, Off
- **Early / late hint**: On, Off
- **Sound**: On, Off
- **Vibration**: On, Off

## Levels

10 levels that unlock in order, shown as a numbered grid with a lock icon on locked ones. The selected level's description appears under the grid:

1. Neon Pulse · Electro · 118 BPM
2. Sunny Side · Funk pop · 102 BPM
3. Pixel Parade · Chiptune · 132 BPM
4. Midnight Drive · Synthwave · 106 BPM
5. Jelly Bounce · Shuffle · 116 BPM
6. Storm Chaser · Drum and bass · 170 BPM
7. Desert Mirage · Eastern scale · 110 BPM
8. Candy Rave · Trance · 148 BPM
9. Iron Gears · Rock · 138 BPM
10. Starlight Finale · Epic · 144 BPM

## Challenges

A collapsible checklist on the start card. When the player completes one, mark it done, save it, and show a short toast:

- Clear any song
- Clear a song with no misses or dropped holds
- Get 50 Perfects in a row
- Complete 10 long notes in one song
- Earn grade S or better
- Clear a song on Hard
- Hit a chord (two notes at once) with Great or better

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
