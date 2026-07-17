# Space Dorito

An arcade-style space shooter built in [PICO-8](https://www.lexaloffle.com/pico-8.php).
Fly a small ship around an open play area and clear waves of targets.

## Gameplay

- Title screen with a drift → flyoff → fade-in transition into gameplay.
- Wave-based target system with a modifier pool: moving targets, multi-hit
  (2-hit / 3-hit) targets, and combinations that scale as waves progress.
- Level system: the map is split into quadrants, and clearing all waves in a
  level advances you to the next map region.
- Scrolling camera and a pulsing radar overlay that tracks nearby targets.

## Controls

| Input | Action |
|-------|--------|
| Arrow keys | Move |
| Z | Shoot |
| X | Boost |

## Running it

Open the `.p8` file in PICO-8:

```
load spacedorito_v1_4_2_merged.p8
run
```

Or drag the cart onto the PICO-8 window.

## Files

- `spacedorito_v1_4_2_merged.p8` — current build (level system, 4 map quadrants).
- `spacedorito_v1_2_3_radar.p8` — earlier single-map build with the radar overlay.

## Development notes

PICO-8 Lua only — no `string.format`, no external libraries, stick to the
built-in API. Screen is fixed 128x128, and carts have hard limits (8192 code
tokens, max compressed size), so new code is kept compact.
