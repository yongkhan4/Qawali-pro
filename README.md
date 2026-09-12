# Qawwali Live v3

GitHub Pages-ready, installable PWA prototype for Android/Chrome.

## Included
- Real-time autocorrelation pitch tracking with confidence gate and note stability
- Scale-aware note locking and tonic selection
- Legato/slide behavior
- Harmonium-style synthesized accompaniment
- Qawwali taal patterns: Keherwa, Dadra, Teentaal
- Tabla, hand-clap and Sa/Pa tanpura-style drone
- Energy controls, Build and Climax
- Low-latency Web Audio routing, gate, reverb and mixer controls
- Stage mode
- Local presets
- Browser latency readout
- Web MIDI capability detection
- Installable PWA shell and offline cache

## Deploy
Upload `index.html`, `manifest.webmanifest`, and `sw.js` to the root of a GitHub Pages repository. Enable Pages from `main` / root. Open the HTTPS Pages URL in Chrome on Android.

## Production caveat
This is the most complete browser prototype that can be delivered as a self-contained artifact here. A truly market-ready commercial product still needs native Android low-latency audio, professionally recorded/licensed harmonium and tabla sample libraries, exhaustive device testing, feedback control, licensing, crash/telemetry strategy, and separate VST3/AU plugin targets.


## v3.1 fix
The previous v3 web build had a JavaScript initialization error because it attempted to attach an event handler to a non-existent `#stop` element. That prevented the Start Live handler from being installed. v3.1 removes that error and registers the service worker/PWA manifest.
