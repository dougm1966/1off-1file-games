# Rink Rivals

[![Rink Rivals](cover.webp)](https://dougm1966.github.io/1off-1file-games/games/rink-rivals/)

**Air hockey, two players on one phone or a CPU ladder.**

▶ **Play:** [https://dougm1966.github.io/1off-1file-games/games/rink-rivals/](https://dougm1966.github.io/1off-1file-games/games/rink-rivals/) · or open [`index.html`](index.html) in any browser

| | |
|---|---|
| Type | Two players |
| Inspired by | air hockey |
| Built for | phones (portrait, touch); also works with mouse and keyboard |

## How it plays

Air hockey on one phone: two players each hold an end, or one player climbs a ten-opponent CPU ladder.

> Knock the puck into the other goal. Solo, work up a ladder of 10 CPU opponents. Two players, hold the phone flat between you, one at each end.

## Controls

Drag your paddle within your half. In two-player mode each person uses their own finger at their own end (multi-touch).

## Settings

| Setting | Options |
|---|---|
| Mode | Vs CPU ladder · Two players |
| First to | 5 · 7 · 11 |
| Puck | Chill · Normal · Fast |

## Levels

1. Rookie
2. Junior
3. Club
4. Varsity
5. Semi-pro
6. Pro
7. All-star
8. Veteran
9. Champion
10. Legend

Levels unlock as you clear them.

## Challenges

A checklist in the menu that saves on your device:

- [ ] Win against the CPU without letting one in
- [ ] Win after being down by 3
- [ ] Score within 3.5 seconds of a faceoff
- [ ] Score with a top-speed shot
- [ ] Beat the Semi-pro
- [ ] Beat the Legend
- [ ] Finish a two-player match

## Look and feel

- Type: Saira Condensed for display, system UI for body text
- Palette: background #0b1220, text #eef5ff, accent #36d1ff
- Layout: logical canvas 360×620, scaled to fit the screen

## Technical notes

- One self-contained HTML file: inline CSS and JavaScript, no build step, no libraries. The only external request is Google Fonts, with system-font fallbacks.
- Settings, unlocked levels, best scores and challenges are stored in the browser's `localStorage`, per device.
- Respects phone safe areas (notches) and never scrolls sideways.
- Recreate or remix it with [`PROMPT.md`](PROMPT.md).
