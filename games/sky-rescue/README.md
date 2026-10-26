# Sky Rescue

**Defender-style rescue shooter.**

▶ **Play:** [https://dougm1966.github.io/1off-1file-games/games/sky-rescue/](https://dougm1966.github.io/1off-1file-games/games/sky-rescue/) · or open [`index.html`](index.html) in any browser

| | |
|---|---|
| Type | Arcade |
| Inspired by | Defender |
| Built for | phones (portrait, touch); also works with mouse and keyboard |

## How it plays

Side-scrolling rescue shooter over a wrap-around world: shoot landers carrying people, catch them as they fall and fly low to set them down. Landers that reach the top become fast mutants.

> Green landers are abducting people. Shoot a lander that's carrying someone, then catch them as they fall and fly low to set them down. If a lander reaches the top, it becomes a fast mutant.

## Controls

Slide up/down to fly, slide left/right to speed up and turn; the laser fires while touching. BOMB clears the screen.

## Settings

| Setting | Options |
|---|---|
| Difficulty | Easy · Standard · Hard |
| Laser | While touching · Always on |

## Levels

1. Wave 1
2. Wave 2
3. Wave 3
4. Wave 4
5. Wave 5
6. Wave 6
7. Wave 7
8. Wave 8
9. Wave 9
10. Wave 10

Levels unlock as you clear them.

## Challenges

A checklist in the menu that saves on your device:

- [ ] Catch a falling person
- [ ] Finish a wave without losing anyone
- [ ] Finish a wave without getting hit
- [ ] Take out 5+ enemies with one bomb
- [ ] Reach wave 5
- [ ] Score 20,000

## Look and feel

- Type: Audiowide for display, system UI for body text
- Palette: background #04030c, text #f0ecff, accent #3dffb0
- Layout: logical canvas 360×600, scaled to fit the screen

## Technical notes

- One self-contained HTML file: inline CSS and JavaScript, no build step, no libraries. The only external request is Google Fonts, with system-font fallbacks.
- Settings, unlocked levels, best scores and challenges are stored in the browser's `localStorage`, per device.
- Respects phone safe areas (notches) and never scrolls sideways.
- Recreate or remix it with [`PROMPT.md`](PROMPT.md).
