# Kart Dash

[![Kart Dash](cover.webp)](https://dougm1966.github.io/1off-1file-games/games/kart-dash/)

**Kart racing with drift boosts and items.**

▶ **Play:** [https://dougm1966.github.io/1off-1file-games/games/kart-dash/](https://dougm1966.github.io/1off-1file-games/games/kart-dash/) · or open [`index.html`](index.html) in any browser

| | |
|---|---|
| Type | Arcade |
| Inspired by | kart racing |
| Built for | phones (portrait, touch); also works with mouse and keyboard |

## How it plays

Top-down kart racing against CPU karts across 9 tracks in 3 cups, with item boxes and drift boosts.

> Race five CPU karts for three laps. Hold ◀ ▶ to steer and GAS to go. Hold DRIFT while turning to slide: blue sparks give a small boost, orange sparks a big one when you let go. Tap the ITEM box on screen to use what you picked up from the ? boxes.

## Controls

◀ ▶ hold buttons on the left; GAS and BRAKE/DRIFT on the right. Hold DRIFT while turning to build a boost, release to fire it. Tap the ITEM box to use an item. Drag-to-steer is a setting.

## Rules and features

- Three CPU difficulties, saved best laps and an optional ghost of your best lap.
- A header mute button and pause button; the game pauses itself when you switch apps.

## Settings

| Setting | Options |
|---|---|
| CPU difficulty | Easy · Normal · Hard |
| Mode | Single race · Cup (3 races) |
| Laps | 2 · 3 · 5 |
| Steering | ◀ ▶ buttons · Drag on board |
| Gas | Hold GAS · Auto-gas |
| Item boxes | On · Off |
| Ghost of best lap | Off · On |
| Controls side | Buttons right · Buttons left |
| Sound | On · Off |
| Vibration | On · Off |

## Levels

1. Sunny Loop · Nut Cup
2. Figure Bay · Nut Cup
3. Pine Hairpin · Nut Cup
4. Canyon Run · Gear Cup
5. Harbor Chicane · Gear Cup
6. Peak Pass · Gear Cup
7. Neon Docks · Star Cup
8. Glacier Switch · Star Cup
9. Grand Circuit · Star Cup

Levels unlock as you clear them.

## Challenges

A checklist in the menu that saves on your device:

- [ ] 1. Sunny Loop: lap --
- [ ] 2. Figure Bay: lap --
- [ ] 3. Pine Hairpin: lap --
- [ ] 4. Canyon Run: lap --
- [ ] 5. Harbor Chicane: lap --
- [ ] 6. Peak Pass: lap --
- [ ] 7. Neon Docks: lap --
- [ ] 8. Glacier Switch: lap --
- [ ] 9. Grand Circuit: lap --
- [ ] Win a race
- [ ] Release an orange-spark drift boost
- [ ] Hit a rival with a Seeker
- [ ] Finish on the podium without touching a wall
- [ ] Win after being in last place
- [ ] Win a cup
- [ ] Win a race on Hard

## Look and feel

- Type: system UI
- Palette: 
- Layout: 

## Technical notes

- One self-contained HTML file: inline CSS and JavaScript, no build step, no libraries. The only external request is Google Fonts, with system-font fallbacks.
- Settings, unlocked levels, best scores and challenges are stored in the browser's `localStorage`, per device.
- Respects phone safe areas (notches) and never scrolls sideways.
- Recreate or remix it with [`PROMPT.md`](PROMPT.md).
