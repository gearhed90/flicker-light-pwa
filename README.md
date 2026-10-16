# Flicker Light PWA

A simple Progressive Web App for stroboscopic light sessions on iPhone (tested conceptually for iOS 18+ / iPhone 15 Pro).

## How to use on iPhone 15 Pro

1. Host these files on any HTTPS server (or use a local tunnel).
2. Open `index.html` in Safari.
3. Tap the Share button → **Add to Home Screen**.
4. Launch the installed app.
5. Choose a mode and tap **Start Session**.
6. Allow camera access if prompted (needed for the torch).
7. Close your eyes and point the back of the phone toward them (or rest it on a pillow as you did with Lumenate).

## Modes

- **Alpha (8–12 Hz)**: Strong geometric closed-eye visuals (the classic range).
- **Theta (4–8 Hz)**: Softer, dreamier feel.
- **Mixed progression**: ~10-minute sequence that steps through useful rates.
- **Custom**: Set any frequency from 2–40 Hz.

## Notes

- The app first tries to control the real flashlight via the MediaStream torch constraint (available on recent iOS).
- If the torch API fails or is blocked, it falls back to pulsing the full screen between black and white.
- Stop immediately if you feel unwell. Not suitable for anyone with photosensitive epilepsy.
- For best results use in a dark room with eyes closed.
- Intensity is highest with the actual torch; screen fallback is weaker but still usable.

## Files

- `index.html` — main app
- `manifest.json` — PWA manifest
- `sw.js` — service worker (basic offline caching)
