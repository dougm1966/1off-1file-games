# Strike Lane

[![Strike Lane](cover.webp)](https://dougm1966.github.io/1off-1file-games/games/strike-lane/)

**Ten-pin bowling, 1–4 players or CPU.**

▶ **Play:** [https://dougm1966.github.io/1off-1file-games/games/strike-lane/](https://dougm1966.github.io/1off-1file-games/games/strike-lane/) · or open [`index.html`](index.html) in any browser

| | |
|---|---|
| Type | Two players |
| Inspired by | ten-pin bowling |
| Built for | phones (portrait, touch); also works with mouse and keyboard |

## How it plays

Ten-pin bowling for 1–4 players or against a CPU, with real pin physics and full scoring including strikes, spares and the 10th frame.

> Drag in the position strip to slide the bowler along the foul line. Then flick up from the release zone: the direction of the flick is your aim, its speed is your power, and a curve at the end of the flick adds hook. Ten pins, ten frames.

## Controls

Drag the strip under the lane to slide the bowler along the foul line, then flick up from the release zone: flick direction aims, speed sets power, and a curve at the end of the flick adds hook.

## Rules and features

- Oil patterns, ball weight, aim guide and a scorecard; a pass card between players.
- A header mute button and pause button; the game pauses itself when you switch apps.

## Settings

| Setting | Options |
|---|---|
| Players (pass and play) | 1 · 2 · 3 · 4 |
| CPU opponent | Off · Casual · Skilled · Pro |
| Oil pattern | Dry · House · Slick |
| Ball weight | 8 lb · 12 lb · 15 lb |
| Game length | 10 frames · 5 frames |
| Aim guide while flicking | On · Off |
| Show last throw path | On · Off |
| Sound | On · Off |
| Vibration | On · Off |

## Challenges

A checklist in the menu that saves on your device:

- [ ] Throw a strike
- [ ] Pick up a spare
- [ ] Three strikes in a row
- [ ] Strike with a strong hook
- [ ] Convert a split
- [ ] Score 150 or more in a game
- [ ] Beat the CPU

## Look and feel

- Type: system UI
- Palette: 
- Layout: 

## Technical notes

- One self-contained HTML file: inline CSS and JavaScript, no build step, no libraries. The only external request is Google Fonts, with system-font fallbacks.
- Settings, unlocked levels, best scores and challenges are stored in the browser's `localStorage`, per device.
- Respects phone safe areas (notches) and never scrolls sideways.
- Recreate or remix it with [`PROMPT.md`](PROMPT.md).
