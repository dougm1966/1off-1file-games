# Garden Crawl

**Centipede-style shooter.**

▶ **Play:** [https://dougm1966.github.io/1off-1file-games/games/garden-crawl/](https://dougm1966.github.io/1off-1file-games/games/garden-crawl/) · or open [`index.html`](index.html) in any browser

| | |
|---|---|
| Type | Arcade |
| Inspired by | Centipede |
| Built for | phones (portrait, touch); also works with mouse and keyboard |

## How it plays

A centipede winds down through a mushroom patch. Each segment you hit becomes a mushroom and splits the train; spiders score more the closer they are.

> A centipede is winding down through the mushroom patch. Shoot every segment. Each hit segment sprouts a new mushroom, and the train splits in two.
> Slide anywhere to move inside the bottom zone. Spiders score more the closer they are when you hit them.

## Controls

Slide anywhere to move inside the bottom zone; the sprayer fires automatically.

## Rules and features

- Mushrooms take four hits.
- Three lives; best score saved.

## Look and feel

- Type: Fredoka for display, system UI for body text
- Palette: background #120d1f, text #f6f0ff, accent #9cff57
- Layout: logical canvas 360×600, scaled to fit the screen

## Technical notes

- One self-contained HTML file: inline CSS and JavaScript, no build step, no libraries. The only external request is Google Fonts, with system-font fallbacks.
- Settings, unlocked levels, best scores and challenges are stored in the browser's `localStorage`, per device.
- Respects phone safe areas (notches) and never scrolls sideways.
- Recreate or remix it with [`PROMPT.md`](PROMPT.md).
