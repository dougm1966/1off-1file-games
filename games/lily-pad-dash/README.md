# Lily Pad Dash

[![Lily Pad Dash](cover.webp)](https://dougm1966.github.io/1off-1file-games/games/lily-pad-dash/)

**Frogger-style road and river crossing.**

▶ **Play:** [https://dougm1966.github.io/1off-1file-games/games/lily-pad-dash/](https://dougm1966.github.io/1off-1file-games/games/lily-pad-dash/) · or open [`index.html`](index.html) in any browser

| | |
|---|---|
| Type | Arcade |
| Inspired by | Frogger |
| Built for | phones (portrait, touch); also works with mouse and keyboard |

## How it plays

Hop a frog across five lanes of traffic and a river of logs and diving turtles into five lily-pad bays. Fill every bay to clear the level. Ten levels add faster lanes, diving turtles and a gator.

> Hop across the road and river and fill all five lily pads. Use the D-pad under the board: each press is one square. You can also swipe on the board.

## Controls

A D-pad under the board: each press is one hop in the direction of the wedge you touch, and the next square is outlined on the board. A big HOP button hops forward. You can also swipe on the board. Arrow keys work too.

## Rules and features

- 10 levels that unlock, and 7 challenges.
- Settings include difficulty, lives, hold-to-keep-hopping and the grid guide.
- A header mute button and pause button; the game pauses itself when you switch apps.

## Settings

| Setting | Options |
|---|---|
| Difficulty | Easy · Normal · Hard |
| Lives | 3 · 5 · 7 |
| Swipe on board | On · Off |
| Tap board to hop forward | On · Off |
| Hold to keep hopping | Off · On |
| Grid guide | On · Off |
| Controls side | Buttons right · Buttons left |
| Sound | On · Off |
| Vibration | On · Off |

## Levels

1. Pond Path
2. Morning Rush
3. Log Jam
4. Diving Turtles
5. Fast Lane
6. Flood Tide
7. Gator Bay
8. Night Traffic
9. Rapids
10. Lily Legend

Levels unlock as you clear them.

## Challenges

A checklist in the menu that saves on your device:

- [ ] Eat a fly in a lily bay
- [ ] Reach a lily pad within 8 seconds
- [ ] Clear a level without losing a frog
- [ ] Clear Fast Lane (level 5)
- [ ] Clear level 3 on Hard
- [ ] Clear Lily Legend
- [ ] Make 500 hops in one game

## Look and feel

- Type: Lilita One + Nunito
- Palette: deep green (#10241a) with a warm yellow accent (#ffd34d); bright cartoon cars, logs, red-shelled turtles
- Layout: canvas 360×520 on a 40px grid

## Technical notes

- One self-contained HTML file: inline CSS and JavaScript, no build step, no libraries. The only external request is Google Fonts, with system-font fallbacks.
- Settings, unlocked levels, best scores and challenges are stored in the browser's `localStorage`, per device.
- Respects phone safe areas (notches) and never scrolls sideways.
- Recreate or remix it with [`PROMPT.md`](PROMPT.md).
