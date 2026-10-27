# Pantry Raid

[![Pantry Raid](cover.webp)](https://dougm1966.github.io/1off-1file-games/games/pantry-raid/)

**Maze chase: mouse vs cats.**

▶ **Play:** [https://dougm1966.github.io/1off-1file-games/games/pantry-raid/](https://dougm1966.github.io/1off-1file-games/games/pantry-raid/) · or open [`index.html`](index.html) in any browser

| | |
|---|---|
| Type | Arcade |
| Inspired by | Pac-Man |
| Built for | phones (portrait, touch); also works with mouse and keyboard |

## How it plays

A mouse eats every crumb in the pantry while cats prowl. Cheese turns the tables. Three maze layouts, 2–4 cats, 10 levels.

> Sneak the mouse through the pantry and eat every crumb. Steer with the D-pad: press a direction early and the mouse turns at the next opening. Cheese makes the cats run, so chase them back to their box.

## Controls

A D-pad under the board. Press a direction early and the mouse turns at the next opening; a small arrow on the mouse shows the waiting turn. Swipe on the board also works (setting).

## Rules and features

- 10 levels that unlock, and 7 challenges.
- A header mute button and pause button; the game pauses itself when you switch apps.

## Settings

| Setting | Options |
|---|---|
| Maze | Classic · Cellar · Shelves |
| Cats | 2 · 3 · 4 |
| Cat speed | Slow · Normal · Fast |
| Lives | 3 · 5 · 7 |
| Swipe on board | On · Off |
| Early turns | Buffered · Instant only |
| Controls side | Buttons right · Buttons left |
| Sound | On · Off |
| Vibration | On · Off |

## Levels

1. Crumb Trail
2. Cheese Please
3. Cat Nap
4. Tail Tip
5. Midnight Snack
6. Pantry Patrol
7. Whisker Walk
8. Cat Cradle
9. Mouse Trap Alley
10. The Big Cheese

Levels unlock as you clear them.

## Challenges

A checklist in the menu that saves on your device:

- [ ] Chase down 3 cats with one cheese
- [ ] Eat a bonus apple
- [ ] Clear a level without being caught
- [ ] Clear a level with Fast cats
- [ ] Score 5000 in one game
- [ ] Clear Midnight Snack (level 5)
- [ ] Clear The Big Cheese

## Look and feel

- Type: Chewy for display, system UI for body text
- Palette: background #1b1410, text #fff4e0, accent #ffcf4a
- Layout: logical canvas 342×378, scaled to fit the screen

## Technical notes

- One self-contained HTML file: inline CSS and JavaScript, no build step, no libraries. The only external request is Google Fonts, with system-font fallbacks.
- Settings, unlocked levels, best scores and challenges are stored in the browser's `localStorage`, per device.
- Respects phone safe areas (notches) and never scrolls sideways.
- Recreate or remix it with [`PROMPT.md`](PROMPT.md).
