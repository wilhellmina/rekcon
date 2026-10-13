# Reckon

[日本語](README.md) | English

A prototype web app that measures toe (and camber) by placing an iPhone against the wheel face.
It exists to find out whether the accuracy is good enough for real use, compared with the usual string-line method.

The name comes from *dead reckoning*: walking around the car with the iPhone in hand is part of the measurement.

## Status

Phase 1 (total toe of the front wheels, and camber one wheel at a time) is done. Accuracy testing on a real car has not started yet.
Phase 2 (repeated measurements, loop-closure test, CSV export) and Phase 3 (all four wheels, thrust line)
are described in [CLAUDE.md](CLAUDE.md) (in Japanese).

## Usage

Toe and camber are measured separately. Choose one at the top of the page, tap “Start sensors” and allow access to motion sensors.

Fix the iPhone to a jig that rests on the rim lip and hold still: it beeps when the reading is recorded.
Remove the case, or keep it the same every time.

**Toe**
1. Fix the iPhone with its long edge along a horizontal bar that touches the rim lip at the front and the rear (you can switch to the short edge in Settings).
   It can lie flat or stand up. Keep the bar as level as you can and press it against the front-left wheel.
2. Once recorded, walk around the front of the car without turning the bar over, and place it on the front-right wheel the same way. It beeps twice and shows the result.
3. Move quickly (within about 15 seconds). The longer the walk takes, the more drift builds up.

**Camber**
1. Put the back of the iPhone against a vertical bar that touches the rim lip at the top and the bottom, with the screen facing away from the car, and place it on the wheel you want to measure. One wheel at a time is fine.
2. Optionally, measure again with the bar upside down. This cancels out how the iPhone is mounted.
3. The slope of the ground adds directly to the result, so measure on level ground.

## Running it

Everything is in one file, `index.html`. There is no build step and no external library.

- Only Safari on iPhone is targeted.
- The UI is in Japanese and English. Switch at the top right (it starts in the language of the device).
- Motion sensors only work over HTTPS. Open it on GitHub Pages: https://wilhellmina.github.io/rekcon/
- The iPhone has no console, so raw sensor values and errors are shown in the debug panel at the bottom of the page.

## Files

| File | Contents |
| --- | --- |
| `index.html` | The app (HTML, CSS and JS) |
| `README.md` | This README in Japanese |
| `CLAUDE.md` | Specification, in Japanese (measurement principle, coordinate system and formulas, features per phase, validation plan) |
