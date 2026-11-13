# Glow & Go v2 — Sensory Light Wall

A touchscreen sensory app modelled on a wall of glowing LED circles. It is made for children with very short attention spans, limited hand precision and different sensory needs.

## Activities
- **Light wall**: any touch lights the nearest circle and softly lights its neighbours. Dragging leaves a glowing trail. After a quiet moment, an optional slow wave of light invites the child to touch again.
- **Drifting light (new)**: one large glowing orb wanders slowly across the dimmed wall, lighting it up as it passes. Touching near it (the target area is very forgiving) makes it bloom and sparkle, and it slows down while a finger follows it. If a touch misses, the orb drifts toward that spot.
- **Follow a light**: one circle glows with a soft halo. Touching anywhere close to it counts as a success. A missed touch makes the light step toward the finger.
- **Magic ball**: a big glowing ball follows the finger and leaves sparkles behind.

## Grown-up settings
To open the settings, **press and hold the ⚙ button for about 1 second**, so a child's quick tap won't open them.
- Circle size (5 steps)
- Brightness (30–100%)
- Movement speed (Still → Lively)
- How long the glow stays
- Colour palette (Rainbow / Cool / Warm / Soft)
- Sound (Off by default; quiet pentatonic chimes)
- Idle wave, helper words, full screen on first touch, and full screen now
- Quick presets: **Calm & soft** and **Bright & lively**

Settings are saved on the device. The app has no network calls, ads, tracking, scores or timers, and no flashing or strobing. It keeps the screen awake while in use (where supported) and respects the system "reduce motion" setting.

## Running it / offline install
Offline support uses a service worker, and service workers only work over **https** or **localhost**. You can open `index.html` directly as a file and it will still run, but it won't install or cache itself that way.

1. Upload this whole folder to any static https host, such as GitHub Pages, Netlify or Cloudflare Pages.
2. Open the address on the tablet once.
   - **iPad (Safari):** Share → *Add to Home Screen*
   - **Android (Chrome):** ⋮ → *Install app*
3. Launch it from the home-screen icon. It opens full screen and works with no internet connection.

To test locally, run `python -m http.server 8000` in this folder, then open `http://localhost:8000`.

When you change any file, bump `VERSION` in `sw.js` so installed copies pick up the update.

**Tip for children:** turn on iPad *Guided Access* or Android *Screen pinning*. These keep the child inside the app.
