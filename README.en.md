# Reckon

[日本語](README.md) | English

A prototype web app that measures toe (and camber) by placing an iPhone against the wheel face.
It exists to find out whether the accuracy is good enough for real use, compared with the usual string-line method.

The name comes from *dead reckoning*: walking around the car with the iPhone in hand is part of the measurement.

## Status

Phase 1 (total toe of the front wheels) is done. Accuracy testing on a real car has not started yet.
Phase 2 (repeated measurements, loop-closure test, CSV export) and Phase 3 (all four wheels, thrust line)
are described in [CLAUDE.md](CLAUDE.md) (in Japanese).

## Usage

The UI is in Japanese.

1. Fix the iPhone to a jig (an L-shaped bracket or flat plate that rests on the rim lip). Remove the case, or keep it the same every time.
2. Open the page in Safari, tap 「センサー開始」 (Start sensors) and allow access to motion sensors.
3. Hold the back of the iPhone against the front-left wheel, with the screen facing away from the car. Hold still, and it beeps once when the reading is recorded.
4. Walk around the front of the car to the front-right wheel and hold it the same way. It beeps twice and shows the result.
5. Move quickly (within about 15 seconds). The longer the walk takes, the more drift builds up.

## Running it

Everything is in one file, `index.html`. There is no build step and no external library.

- Only Safari on iPhone is targeted.
- Motion sensors only work over HTTPS. Open it on GitHub Pages: https://wilhellmina.github.io/rekcon/
- The iPhone has no console, so raw sensor values and errors are shown in the debug panel at the bottom of the page.

## Files

| File | Contents |
| --- | --- |
| `index.html` | The app (HTML, CSS and JS) |
| `README.md` | This README in Japanese |
| `CLAUDE.md` | Specification, in Japanese (measurement principle, coordinate system and formulas, features per phase, validation plan) |
