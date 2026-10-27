# Immune Response

[![Immune Response](cover.webp)](https://dougm1966.github.io/1off-1file-games/games/immune-response/)

**Immune-system tower defense.**

▶ **Play:** [https://dougm1966.github.io/1off-1file-games/games/immune-response/](https://dougm1966.github.io/1off-1file-games/games/immune-response/) · or open [`index.html`](index.html) in any browser

| | |
|---|---|
| Type | Lab |
| Inspired by | tower defense |
| Built for | phones (portrait, touch); also works with mouse and keyboard |

## How it plays

Defend an organ from waves of bacteria, viruses and fungi by placing immune cells along the vessel: neutrophils, macrophages, NK cells, B cells and T helpers. Ten levels with different vessel layouts.

> Germs travel along the blood vessel to the organ. Tap a glowing spot to build an immune cell, tap a cell to upgrade or sell it, and press NEXT WAVE when ready. Stars 0/30.

## Controls

Tap an empty build spot to open a card of cells with their costs; tap a placed cell to upgrade, sell or change its target. Speed, Fever and Next wave buttons sit under the board.

## Rules and features

- Three difficulties and 7 challenges.
- A header mute button and pause button; the game pauses itself when you switch apps.

## Settings

| Setting | Options |
|---|---|
| Difficulty | Easy · Normal · Hard |
| Mode | Campaign · Endless |
| Auto-send next wave | Off · On |
| Start speed | 1× · 2× |
| New cells target | First · Strong · Weak · Last |
| Range circles | Selected · All · Off |
| Health bars | On · Off |
| Damage numbers | On · Off |
| Controls side | Buttons right · Buttons left |
| Sound | On · Off |
| Vibration | On · Off |

## Levels

1. Paper Cut
2. Sore Throat
3. Gut Instinct
4. Flu Season
5. Kidney Stand
6. Thrush
7. Lung Siege
8. Liver Gate
9. Brain Barrier
10. Sepsis Storm

Levels unlock as you clear them.

## Challenges

A checklist in the menu that saves on your device:

- [ ] Neutrophil - first responder; fast, cheap, great vs bacteria.
- [ ] Macrophage - big eater; engulfs groups of bacteria and fungi.
- [ ] NK cell - kills infected cells; best vs viruses.
- [ ] B cell - antibodies tag germs (blue Y), slowing them and making them take more damage.
- [ ] T helper - releases cytokines that speed up and strengthen nearby cells.
- [ ] Fever - slows every germ for 8 seconds.
- [ ] Armour (TB, MRSA, mold) - big hits work best.
- [ ] Splitters (Strep, Candida) - break into smaller germs when killed.
- [ ] Tap a germ to learn about it.
- [ ] Clear a level without losing organ health
- [ ] Clear a level using only innate cells (no B or T cells)
- [ ] Have one T helper boosting 3 cells at once
- [ ] Kill 40 antibody-marked germs in one game
- [ ] Trigger a Fever while 10+ germs are on screen
- [ ] Clear level 5 on Hard
- [ ] Clear Sepsis Storm (level 10)

## Look and feel

- Type: system UI
- Palette: 
- Layout: 

## Technical notes

- One self-contained HTML file: inline CSS and JavaScript, no build step, no libraries. The only external request is Google Fonts, with system-font fallbacks.
- Settings, unlocked levels, best scores and challenges are stored in the browser's `localStorage`, per device.
- Respects phone safe areas (notches) and never scrolls sideways.
- Recreate or remix it with [`PROMPT.md`](PROMPT.md).
