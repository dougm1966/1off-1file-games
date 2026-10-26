# Sky Hopper

**Endless bounce-and-climb jumper.**

▶ **Play:** [https://dougm1966.github.io/1off-1file-games/games/sky-hopper/](https://dougm1966.github.io/1off-1file-games/games/sky-hopper/) · or open [`index.html`](index.html) in any browser

| | |
|---|---|
| Type | Arcade |
| Inspired by | Doodle Jump-style climber (original character) |
| Built for | phones (portrait, touch); also works with mouse and keyboard |

## How it plays

Bounce from platform to platform and climb as high as you can. Blue platforms slide, brown ones crack, white ones vanish after a bounce; springs, propeller hats and stompable gremlins.

> Bounce from platform to platform and climb as high as you can. Springs launch you, propeller hats fly you up, and you can stomp gremlins from above. Blue platforms slide, brown ones crack, white ones vanish after one bounce.

## Controls

Slide left or right to steer; the hopper bounces automatically and wraps around the screen edges.

## Settings

| Setting | Options |
|---|---|
| Difficulty | Easy · Normal · Hard |
| Gremlins | On · Off |
| Propeller hats | On · Off |
| Hopper | Blue · Orange · Mint |

## Challenges

A checklist in the menu that saves on your device:

- [ ] Reach height 1,000
- [ ] Reach height 2,500
- [ ] Reach height 5,000
- [ ] Hit 5 springs in one run
- [ ] Grab a propeller hat
- [ ] Stomp a gremlin
- [ ] Collect 15 coins in one run

## Look and feel

- Type: Gochi Hand for display, system UI for body text
- Palette: background #fbf6e9, text #2b2a33, accent #3aa3ff
- Layout: logical canvas 360×620, scaled to fit the screen

## Technical notes

- One self-contained HTML file: inline CSS and JavaScript, no build step, no libraries. The only external request is Google Fonts, with system-font fallbacks.
- Settings, unlocked levels, best scores and challenges are stored in the browser's `localStorage`, per device.
- Respects phone safe areas (notches) and never scrolls sideways.
- Recreate or remix it with [`PROMPT.md`](PROMPT.md).
