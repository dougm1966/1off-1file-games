# Ghost Protocol

[![Ghost Protocol](cover.webp)](https://dougm1966.github.io/1off-1file-games/games/ghost-protocol/)

**Top-down stealth infiltration.**

▶ **Play:** [https://dougm1966.github.io/1off-1file-games/games/ghost-protocol/](https://dougm1966.github.io/1off-1file-games/games/ghost-protocol/) · or open [`index.html`](index.html) in any browser

| | |
|---|---|
| Type | Arcade |
| Inspired by | top-down stealth games |
| Built for | phones (portrait, touch); also works with mouse and keyboard |

## How it plays

Sneak through 10 guarded facilities past patrols with visible vision cones, cameras, locked doors and keycards. Rated on time, staying unseen and avoiding takedowns.

> Slip past the guards, download the intel, and reach the exit. Push the stick lightly (inside the dashed ring) to sneak silently; push past the ring to run, which makes noise. TAKEDOWN works only from behind. HIDE/USE hides in lockers and hacks terminals (hold). Stars 0/30.

## Controls

A thumb stick moves you: a light push sneaks silently, a full push runs and makes a visible noise ring. TAKEDOWN and HIDE/USE buttons on the right.

## Rules and features

- Guard alertness, vision-cone visibility and sneak assist settings; 7 challenges.
- A header mute button and pause button; the game pauses itself when you switch apps.

## Settings

| Setting | Options |
|---|---|
| Guard alertness | Relaxed · Normal · Sharp |
| Vision cones | Bright · Soft · Outline |
| Sneak assist | Off · Near guards · Always sneak |
| Takedown aim assist | On · Off |
| Noise ring when running | On · Off |
| Controls side | Buttons right · Buttons left |
| Sound | On · Off |
| Vibration | On · Off |

## Levels

1. First Night
2. Loading Dock
3. Server Farm
4. Atrium
5. Cell Block
6. Control Room
7. Shelf Maze
8. The Vault
9. Rooftop
10. Ghost Protocol

Levels unlock as you clear them.

## Challenges

A checklist in the menu that saves on your device:

- [ ] Clear a level without ever being spotted
- [ ] Clear a level under its par time
- [ ] Take down 3 guards in one level
- [ ] Hide and shake off a guard who was chasing you
- [ ] Blind the cameras at a switch
- [ ] Clear a level without ever running
- [ ] Clear Ghost Protocol (level 10)

## Look and feel

- Type: system UI
- Palette: 
- Layout: 

## Technical notes

- One self-contained HTML file: inline CSS and JavaScript, no build step, no libraries. The only external request is Google Fonts, with system-font fallbacks.
- Settings, unlocked levels, best scores and challenges are stored in the browser's `localStorage`, per device.
- Respects phone safe areas (notches) and never scrolls sideways.
- Recreate or remix it with [`PROMPT.md`](PROMPT.md).
