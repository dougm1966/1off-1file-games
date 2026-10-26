# Pocket Puzzle Duel

**Pass-and-play pool trick-shot puzzles.**

▶ **Play:** [https://dougm1966.github.io/1off-1file-games/games/pocket-puzzle-duel/](https://dougm1966.github.io/1off-1file-games/games/pocket-puzzle-duel/) · or open [`index.html`](index.html) in any browser

| | |
|---|---|
| Type | Two players |
| Inspired by | pool trick-shot puzzles |
| Built for | phones (portrait, touch); also works with mouse and keyboard |

## How it plays

Two players take turns shooting the same pool table layout. Clear every ball in the fewest strokes, golf style, across six holes that add rails, bumper posts, a full rack and a gate of posts.

> Same table layout for both of you. Clear it in the fewest strokes. Lowest total after six holes wins.

## Controls

Slide a finger left or right anywhere on the table to rotate the cue (it never snaps to your finger). ‹ › buttons fine-tune the angle. Set power with the slider and tap Shoot.

## Rules and features

- Six holes with par values; a scratch costs +1 stroke; each hole has a stroke cap.
- The breaker alternates every hole; a hand-off screen says whose turn it is.
- Aim guide shows a dashed line to the first thing the cue ball touches plus a faint ghost ball, but not where balls go after contact.
- Match progress is saved between turns.

## Look and feel

- Type: Bungee (display) + Barlow / Barlow Condensed
- Palette: dark blue-green pool hall (#0d1317), tournament-blue cloth, walnut rails, brass accent (#d9a845)
- Layout: portrait canvas table 452×812

## Technical notes

- One self-contained HTML file: inline CSS and JavaScript, no build step, no libraries. The only external request is Google Fonts, with system-font fallbacks.
- Settings, unlocked levels, best scores and challenges are stored in the browser's `localStorage`, per device.
- Respects phone safe areas (notches) and never scrolls sideways.
- Recreate or remix it with [`PROMPT.md`](PROMPT.md).
