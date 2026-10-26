# Deep Dig

**Tunnel digging and monster popping.**

▶ **Play:** [https://dougm1966.github.io/1off-1file-games/games/deep-dig/](https://dougm1966.github.io/1off-1file-games/games/deep-dig/) · or open [`index.html`](index.html) in any browser

| | |
|---|---|
| Type | Arcade |
| Inspired by | Dig Dug-style tunneling (original characters) |
| Built for | phones (portrait, touch); also works with mouse and keyboard |

## How it plays

Tunnel through layered dirt and pop every monster: pump one four times to burst it, or drop a rock on it for a big bonus. Monsters can drift through dirt as ghostly eyes.

> Tunnel through the dirt and pop every monster. Pump one four times to burst it, or drop a rock on it for a big bonus. Monsters can drift through dirt as ghostly eyes.
> Hold a finger down and slide toward where you want to dig. Tap PUMP while facing a monster up to three tiles away.

## Controls

Hold a finger down and slide toward where you want to dig; tap PUMP while facing a monster up to three tiles away.

## Rules and features

- Deeper layers pay more per monster.
- Three lives; best score saved.

## Look and feel

- Type: Luckiest Guy for display, system UI for body text
- Palette: background #170f0a, text #fff3df, accent #ffb92e
- Layout: logical canvas 364×442, scaled to fit the screen

## Technical notes

- One self-contained HTML file: inline CSS and JavaScript, no build step, no libraries. The only external request is Google Fonts, with system-font fallbacks.
- Settings, unlocked levels, best scores and challenges are stored in the browser's `localStorage`, per device.
- Respects phone safe areas (notches) and never scrolls sideways.
- Recreate or remix it with [`PROMPT.md`](PROMPT.md).
