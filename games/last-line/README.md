# Last Line

**Missile Command-style city defense.**

▶ **Play:** [https://dougm1966.github.io/1off-1file-games/games/last-line/](https://dougm1966.github.io/1off-1file-games/games/last-line/) · or open [`index.html`](index.html) in any browser

| | |
|---|---|
| Type | Arcade |
| Inspired by | Missile Command |
| Built for | phones (portrait, touch); also works with mouse and keyboard |

## How it plays

Defend six cities from falling missiles by bursting counter-missiles in the sky. Some missiles split later in the game.

> Missiles are falling on your six cities. Tap the sky to burst a counter-missile there. Lead your shots, because blasts take a moment to grow.
> The nearest base with ammo fires. Leftover ammo and surviving cities pay a bonus.

## Controls

Tap the sky where you want a burst; the nearest base with ammo fires.

## Rules and features

- Leftover ammo and surviving cities pay a bonus each wave.
- Game ends when every city is gone.

## Look and feel

- Type: Teko for display, system UI for body text
- Palette: background #0a0716, text #fff1e8, accent #ffcc33
- Layout: logical canvas 360×600, scaled to fit the screen

## Technical notes

- One self-contained HTML file: inline CSS and JavaScript, no build step, no libraries. The only external request is Google Fonts, with system-font fallbacks.
- Settings, unlocked levels, best scores and challenges are stored in the browser's `localStorage`, per device.
- Respects phone safe areas (notches) and never scrolls sideways.
- Recreate or remix it with [`PROMPT.md`](PROMPT.md).
