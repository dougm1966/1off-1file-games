# Lab Letters

**Five-letter word guessing with lab words or partner-set words.**

▶ **Play:** [https://dougm1966.github.io/1off-1file-games/games/lab-letters/](https://dougm1966.github.io/1off-1file-games/games/lab-letters/) · or open [`index.html`](index.html) in any browser

| | |
|---|---|
| Type | Lab |
| Inspired by | Wordle |
| Built for | phones (portrait, touch); also works with mouse and keyboard |

## How it plays

Guess the five-letter lab word in six tries. Tiles show which letters are in the right spot or in the word.

> Guess the hidden five-letter word. Green means right letter, right spot. Gold means right letter, wrong spot. The lab list is all bench and body words. In Partner mode, one of you sets a word for the other.

## Controls

Type with the on-screen keyboard (or a physical keyboard) and press Enter.

## Settings

| Setting | Options |
|---|---|
| Words | Lab & body words · Partner sets the word |
| Guesses | 6 · 8 · easier |
| Hard mode | Off · Must reuse hints |

## Challenges

A checklist in the menu that saves on your device:

- [ ] Solve a word
- [ ] Solve in 2 guesses
- [ ] Solve 5 in a row
- [ ] Solve in hard mode
- [ ] Solve a word your partner set
- [ ] Solve 10 words total

## Look and feel

- Type: Roboto Slab for display, system UI for body text
- Palette: background #121417, text #f2f4f7, accent #5fb27a
- Layout: logical canvas 360×600, scaled to fit the screen

## Technical notes

- One self-contained HTML file: inline CSS and JavaScript, no build step, no libraries. The only external request is Google Fonts, with system-font fallbacks.
- Settings, unlocked levels, best scores and challenges are stored in the browser's `localStorage`, per device.
- Respects phone safe areas (notches) and never scrolls sideways.
- Recreate or remix it with [`PROMPT.md`](PROMPT.md).
