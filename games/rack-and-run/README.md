# Rack & Run

**9-ball pool with real rules, friend or CPU.**

▶ **Play:** [https://dougm1966.github.io/1off-1file-games/games/rack-and-run/](https://dougm1966.github.io/1off-1file-games/games/rack-and-run/) · or open [`index.html`](index.html) in any browser

| | |
|---|---|
| Type | Two players |
| Inspired by | 9-ball pool |
| Built for | phones (portrait, touch); also works with mouse and keyboard |

## How it plays

Real 9-ball rules: hit the lowest-numbered ball first, pocket balls to keep shooting, legally pocket the 9 to win the rack. Fouls give the opponent ball in hand.

> Real 9-ball. Hit the lowest-numbered ball first. Sink anything legally to keep shooting. Legally pocket the 9 to win the rack. Fouls give your opponent ball in hand.

## Controls

Slide on the table to rotate the cue, ‹ › to fine-tune, power slider, Shoot. During ball in hand, drag the cue ball, then tap Set ball.

## Settings

| Setting | Options |
|---|---|
| Opponent | Pass & play · CPU easy · CPU hard |
| Race to | 3 · 5 · 7 |
| Aim guide | Full · Contact only · Short line |
| Break | Alternate · Winner breaks |

## Challenges

A checklist in the menu that saves on your device:

- [ ] Win a rack
- [ ] Break and run out a rack
- [ ] Make the 9 on the break
- [ ] Win a rack on a combo into the 9
- [ ] Win a race to 7
- [ ] Beat the hard CPU

## Look and feel

- Type: Bungee for display, system UI for body text
- Palette: background #0d1317, text #e9eef1, accent #d9a845
- Layout: logical canvas 452×812, scaled to fit the screen

## Technical notes

- One self-contained HTML file: inline CSS and JavaScript, no build step, no libraries. The only external request is Google Fonts, with system-font fallbacks.
- Settings, unlocked levels, best scores and challenges are stored in the browser's `localStorage`, per device.
- Respects phone safe areas (notches) and never scrolls sideways.
- Recreate or remix it with [`PROMPT.md`](PROMPT.md).
