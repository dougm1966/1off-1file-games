# Bench Rounds

[![Bench Rounds](cover.webp)](https://dougm1966.github.io/1off-1file-games/games/bench-rounds/)

**Clinical lab trivia, solo or pass-and-play.**

▶ **Play:** [https://dougm1966.github.io/1off-1file-games/games/bench-rounds/](https://dougm1966.github.io/1off-1file-games/games/bench-rounds/) · or open [`index.html`](index.html) in any browser

| | |
|---|---|
| Type | Lab |
| Inspired by | clinical lab trivia |
| Built for | phones (portrait, touch); also works with mouse and keyboard |

## How it plays

Clinical laboratory trivia across the benches: hematology, chemistry, microbiology, blood bank, urinalysis, coag and specimen handling. Solo or pass-and-play for 2–4.

> Clinical lab trivia across seven benches. Read the question, then tap one of the four big answer buttons. Solo, or pass the phone around with 2 to 4 players.

## Controls

Big full-width answer buttons. Each answer shows an explanation; tap Next to continue.

## Rules and features

- Settings for categories, difficulty, question count and timer.
- A header mute button and pause button; the game pauses itself when you switch apps.

## Settings

| Setting | Options |
|---|---|
| Players | Solo · 2 · 3 · 4 |
| Difficulty | Easy · Mixed · Hard · Ramp up |
| Questions each | 5 · 10 · 15 · 20 |
| Clock per question | Off · 15 s · 20 s · 30 s |
| Benches | All seven · Pick… |
| Sound | On · Off |
| Vibration | On · Off |

## Challenges

A checklist in the menu that saves on your device:

- [ ] Answer 5 in a row correctly
- [ ] Answer correctly within 3 seconds (clock on)
- [ ] Finish a solo round of 5+ questions with none wrong
- [ ] Get 5 Hard questions right in one round
- [ ] Get a question right on every bench
- [ ] Finish a game with 3 or 4 players
- [ ] Finish a 20-question round

## Look and feel

- Type: IBM Plex Sans / Condensed / Mono
- Palette: specimen-label cards; light and dark themes; category colors match tube caps (lavender, light blue, gold, green, pink, yellow, gray)
- Layout: HTML/CSS cards, no canvas

## Technical notes

- One self-contained HTML file: inline CSS and JavaScript, no build step, no libraries. The only external request is Google Fonts, with system-font fallbacks.
- Settings, unlocked levels, best scores and challenges are stored in the browser's `localStorage`, per device.
- Respects phone safe areas (notches) and never scrolls sideways.
- Recreate or remix it with [`PROMPT.md`](PROMPT.md).
