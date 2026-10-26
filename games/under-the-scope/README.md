# Under the Scope

**Identify blood smears, Gram stains and urine sediment.**

▶ **Play:** [https://dougm1966.github.io/1off-1file-games/games/under-the-scope/](https://dougm1966.github.io/1off-1file-games/games/under-the-scope/) · or open [`index.html`](index.html) in any browser

| | |
|---|---|
| Type | Lab |
| Inspired by | microscope slide identification |
| Built for | phones (portrait, touch); also works with mouse and keyboard |

## How it plays

Identify what you see in a drawn microscope field: 27 specimens across red-cell morphology, white cells, Gram and acid-fast stains, and urine sediment. Each look is a freshly randomized field with realistic stain backgrounds, platelets, debris and refractile crystals.

## Controls

Tap the answer. Another view redraws the same specimen with a new random field.

## Rules and features

- Difficulty: Student (slide type shown, 4 choices, no clock), Tech (slide type hidden, 25 s clock), Pathologist (6 choices from any bench, 15 s clock).
- Solo or pass-and-play for two; streak bonuses.
- Every answer explains the key identifying features.

## Look and feel

- Type: IBM Plex Sans / Condensed / Mono
- Palette: dark UI (#0e1114) around a circular eyepiece with vignette and grain; Wright-stain pinks/purples, Gram stain pinks/purples, blue AFB counterstain, beige unstained urine
- Layout: canvas 760×760 eyepiece

## Technical notes

- One self-contained HTML file: inline CSS and JavaScript, no build step, no libraries. The only external request is Google Fonts, with system-font fallbacks.
- Settings, unlocked levels, best scores and challenges are stored in the browser's `localStorage`, per device.
- Respects phone safe areas (notches) and never scrolls sideways.
- Recreate or remix it with [`PROMPT.md`](PROMPT.md).
