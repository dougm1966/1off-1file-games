# Swarm Wing

[![Swarm Wing](cover.webp)](https://dougm1966.github.io/1off-1file-games/games/swarm-wing/)

**Galaga-style swooping shooter.**

▶ **Play:** [https://dougm1966.github.io/1off-1file-games/games/swarm-wing/](https://dougm1966.github.io/1off-1file-games/games/swarm-wing/) · or open [`index.html`](index.html) in any browser

| | |
|---|---|
| Type | Arcade |
| Inspired by | Galaga |
| Built for | phones (portrait, touch); also works with mouse and keyboard |

## How it plays

Shoot down swooping waves of insect-like ships over 10 stages, including no-return-fire challenge stages. Catch a wingman capsule for a twin ship; a hit costs the wingman before it costs a life.

> The swarm loops in, forms up, then peels off to dive at you. Hold ◀ ▶ to move and the big FIRE button to shoot, at the same time. Diving hits score double. Catch the cyan capsule for a wingman.

## Controls

◀ ▶ hold buttons and a FIRE button, usable together. Auto-fire and a 'Drag ship' mode are settings.

## Rules and features

- 10 stages that unlock, and 7 challenges.
- A header mute button and pause button; the game pauses itself when you switch apps.

## Settings

| Setting | Options |
|---|---|
| Difficulty | Easy · Normal · Hard |
| Controls | ◀ ▶ + FIRE · Drag ship |
| Auto-fire (buttons mode) | Off · On |
| Lives | 3 · 5 |
| Challenge stages | On · Off |
| Controls side | Buttons right · Buttons left |
| Sound | On · Off |
| Vibration | On · Off |

## Levels

1. Warm-up
2. Swoop
3. Pincer
4. Challenge I
5. Dive Bombers
6. Crossfire
7. Leaders' Guard
8. Challenge II
9. Storm
10. Final Swarm

Levels unlock as you clear them.

## Challenges

A checklist in the menu that saves on your device:

- [ ] Clear stage 1
- [ ] Catch a wingman capsule
- [ ] Shoot 8 diving enemies in one stage
- [ ] Clear a stage without losing a ship
- [ ] Hit 30 of 40 in a challenge stage
- [ ] Perfect a challenge stage (40 of 40)
- [ ] Clear the Final Swarm (stage 10)

## Look and feel

- Type: Exo 2 for display, system UI for body text
- Palette: background #06040f, text #f1ecff, accent #ffd23f
- Layout: logical canvas 360×620, scaled to fit the screen

## Technical notes

- One self-contained HTML file: inline CSS and JavaScript, no build step, no libraries. The only external request is Google Fonts, with system-font fallbacks.
- Settings, unlocked levels, best scores and challenges are stored in the browser's `localStorage`, per device.
- Respects phone safe areas (notches) and never scrolls sideways.
- Recreate or remix it with [`PROMPT.md`](PROMPT.md).
