# Color Match

See a color for a few seconds, then dial it back in from memory. A phone-friendly color memory game in the spirit of [Dialed](https://dialed.gg), with no ads and no account.

**Play:** https://ykbarros.github.io/color-match/

## How it plays
- A color fills the screen for **5 seconds** (Easy) or **2 seconds** (Hard).
- Rebuild it with **hue**, **saturation** and **brightness** sliders, then lock it in.
- Each color scores **0–10** by how different the two look to the eye (CIEDE2000), so a hue miss on a vivid color costs more than the same miss on a near-grey. Five colors per game, 50 max.

## Modes
- **Daily:** the same five colors for everyone, every day. Progress saves after each color, so closing the tab mid-game resumes where you left off (and you don't get a second look at a color you already saw). Tracks your streak, best and average.
- **Practice:** five fresh colors every game, as many as you like.
- **Challenges:** *Share* on a practice result sends a link with your exact five colors and score, so a friend can try to beat it.

## On your phone
Open the link and use **Add to Home Screen** (Safari share menu, or Chrome's *Install app*). It launches full screen like an app and works offline after the first visit.

## Files
- `index.html`: the whole game: markup, styles and script, no build step.
- `sw.js`: offline cache. It opens from cache and refreshes in the background, so after you push a change, phones show it on their second launch.
- `manifest.webmanifest` and `icon-*.png`: home-screen install.

Stats live in the browser's `localStorage`, so they're per device.
