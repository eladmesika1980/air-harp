# Air Harp 🎶

Play glowing strings in the air with your webcam. Hand tracking runs entirely in the browser — no video leaves your device.

**Live:** https://eladmesika1980.github.io/air-harp/

## How it works
- **Hand tracking:** [MediaPipe Hand Landmarker](https://ai.google.dev/edge/mediapipe/solutions/vision/hand_landmarker) (21 landmarks per hand, WebAssembly + WebGL)
- **Pluck detection:** a fingertip's path between frames crossing a string segment
- **Sound:** Karplus-Strong plucked-string synthesis in the Web Audio API, with convolution reverb
- **Visuals:** Canvas 2D

## On a phone
- Prop the phone up facing you; the front camera is used.
- iPhone: turn off silent mode, or Web Audio stays muted.
- Settings sit behind the ⚙️ button (collapsed on narrow screens). The screen stays awake while playing, where the browser supports it.

## Run locally
Open `index.html` in Chrome, or serve it (e.g. VS Code Live Server). The camera needs `https` or `localhost`.
