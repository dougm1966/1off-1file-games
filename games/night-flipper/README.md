# Night Flipper

**Neon pinball with missions.**

▶ **Play:** [https://dougm1966.github.io/1off-1file-games/games/night-flipper/](https://dougm1966.github.io/1off-1file-games/games/night-flipper/) · or open [`index.html`](index.html) in any browser

| | |
|---|---|
| Type | Arcade |
| Inspired by | pinball |
| Built for | phones (portrait, touch); also works with mouse and keyboard |

## How it plays

A neon table with bumpers, slingshots, drop targets and top lanes. Rotating missions raise your multiplier and every second mission lights multiball.

> Keep the ball alive and work through the missions shown mid-table. Each one raises your multiplier. Every second mission lights multiball.

## Controls

Hold the left or right half of the screen for each flipper (multi-touch). Hold, then release to launch; release at NOW for the skill shot.

## Settings

| Setting | Options |
|---|---|
| Table slope | Gentle · Standard · Steep |
| Balls | 3 · 5 |
| Ball save | Long · Short · Off |
| Multiball | On · Off |

## Challenges

A checklist in the menu that saves on your device:

- [ ] Hit the skill shot (release at NOW)
- [ ] Light all 3 top lanes
- [ ] Complete 3 missions in one game
- [ ] Complete 5 missions in one game
- [ ] Start multiball
- [ ] 100 bumper hits in one game
- [ ] Score 50,000
- [ ] Score 150,000

## Look and feel

- Type: Monoton for display, system UI for body text
- Palette: background #0b0618, text #fbefff, accent #ff4fd8
- Layout: logical canvas 340×640, scaled to fit the screen

## Technical notes

- One self-contained HTML file: inline CSS and JavaScript, no build step, no libraries. The only external request is Google Fonts, with system-font fallbacks.
- Settings, unlocked levels, best scores and challenges are stored in the browser's `localStorage`, per device.
- Respects phone safe areas (notches) and never scrolls sideways.
- Recreate or remix it with [`PROMPT.md`](PROMPT.md).
