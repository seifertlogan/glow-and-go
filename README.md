# Glow & Go — older iPad version

This is a copy of `glow-and-go-app` changed to run on older iPads that can't update past **iOS 12** (for example, the first-generation iPad Air). Use the main `glow-and-go-app` folder for all other devices.

## What's different from the main app
- **Touch input:** uses touch events (plus mouse, for testing on a computer), because Safari 12 has no Pointer Events. This was the main reason taps did nothing.
- **Settings button:** press-and-hold on ⚙ also uses touch events.
- **Sound:** changes the audio wiring to the form Safari 12 accepts.
- **Layout:** replaces newer CSS (`inset`, flexbox `gap`, `dvh`, unprefixed `sticky`) with older equivalents.
- **Performance:** draws at standard resolution instead of Retina, so the animation stays smooth on the older chip.
- **Offline cache:** uses its own cache name (`glow-and-go-legacy-…`), so it can be hosted beside the main app without the two interfering.

## Extra features (this version only)
- **Background music:** Off / Calm pads / Music box / Ocean waves, with a volume slider (Very quiet → Medium). The music is generated on the device, so it works offline. It fades in slowly, has no sudden sounds, and starts at the child's first touch, because iPads only allow sound after a touch. The iPad's side mute switch silences it.
- **Child lock:** hides the ⚙ button almost completely. To unlock, press and hold the top-right corner still for 3 seconds. A sliding finger cancels the hold, so a child playing won't open it. For a full lock that also blocks the Home button, use iPad **Guided Access** (Settings → General → Accessibility → Guided Access, then triple-click the Home button inside the app).

Activities, settings and behaviour are otherwise identical. If you change the main app, copy the change here too and bump `VERSION` in `sw.js`.

## Putting it on the iPad
1. Host this folder on https (e.g. GitHub Pages), next to the main app — for example `…/glow-and-go-app/` and `…/glow-and-go-ipad-legacy/`.
2. On the iPad, open the legacy address in Safari → Share → **Add to Home Screen**.
3. Launch from the home-screen icon.

To test on your computer: run `python -m http.server 8000` in this folder and open `http://localhost:8000`.
