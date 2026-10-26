# Eight & Out

**8-ball pool, friend or CPU.**

▶ **Play:** [https://dougm1966.github.io/1off-1file-games/games/eight-and-out/](https://dougm1966.github.io/1off-1file-games/games/eight-and-out/) · or open [`index.html`](index.html) in any browser

| | |
|---|---|
| Type | Two players |
| Inspired by | 8-ball pool |
| Built for | phones (portrait, touch); also works with mouse and keyboard |

## How it plays

8-ball with solids and stripes, open-table rules, fouls and ball in hand. Sink your group, then the 8.

> 8-ball. The table is open after the break. The first ball you legally sink makes you solids or stripes. Clear your group, then sink the 8 to win. Sink the 8 early or scratch on it and you lose the rack.

## Controls

Slide on the table to aim, fine-tune buttons, power slider and Shoot; drag the cue ball during ball in hand.

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
- [ ] Run all 7 of your group in one turn
- [ ] Win a race to 7
- [ ] Beat the hard CPU

## Look and feel

- Type: Bungee for display, system UI for body text
- Palette: background #0d1317, text #e9eef1, accent #e0604a
- Layout: logical canvas 452×812, scaled to fit the screen

## Technical notes

- One self-contained HTML file: inline CSS and JavaScript, no build step, no libraries. The only external request is Google Fonts, with system-font fallbacks.
- Settings, unlocked levels, best scores and challenges are stored in the browser's `localStorage`, per device.
- Respects phone safe areas (notches) and never scrolls sideways.
- Recreate or remix it with [`PROMPT.md`](PROMPT.md).
