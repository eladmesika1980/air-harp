# Air Harp 🎶

Play glowing strings in the air with your webcam. Hand tracking runs entirely in the browser — no video leaves your device.

**Live:** https://eladmesika1980.github.io/air-harp/

## How it works
- **Hand tracking:** [MediaPipe Hand Landmarker](https://ai.google.dev/edge/mediapipe/solutions/vision/hand_landmarker) (21 landmarks per hand, WebAssembly + WebGL)
- **Pluck detection:** a fingertip's path between frames crossing a string segment
- **Tuning by length:** pinch (thumb + index) a string's free end and stretch or shorten it. Long = low, short = high,
  linear per semitone (E2–E5) so high strings stay pluckable. Snaps to the chosen scale unless "free tuning" is on.
  The tuning is saved in the browser (`localStorage`); "reset tuning" or changing the scale restores the defaults.
- **Strings:** 6 by default; 4–9 in settings (changing the count resets the tuning).
- **Sound:** six sound types, all synthesized in the Web Audio API (no samples), through a shared filter, convolution reverb and compressor:
  harp and oud/guitar (Karplus-Strong plucked string), kalimba and marimba (decaying sine partials),
  bells (FM synthesis), synth (detuned sawtooths through a sweeping low-pass). Saved with the tuning.
- **Defaults:** synth sound, and every fingertip plucks (the "all fingers" box is on).
- **Visuals:** Canvas 2D

## On a phone
- Prop the phone up facing you; the front camera is used.
- iPhone: turn off silent mode, or Web Audio stays muted.
- Settings sit behind the ⚙️ button (collapsed on narrow screens). The screen stays awake while playing, where the browser supports it.

## Run locally
Open `index.html` in Chrome, or serve it (e.g. VS Code Live Server). The camera needs `https` or `localhost`.
