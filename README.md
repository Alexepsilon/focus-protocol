# Focus Protocol

A single-file study-focus sound app with a timed protocol. No build step, no dependencies, works offline, installable on a phone.

**Live:** https://alexepsilon.github.io/focus-protocol/

## What it does
- **Protocols** – timed study sessions (Deep work 50/10, Pomodoro 25/5, Memorise/Recall, Exam sprint, Monroe wind-down, Custom). Each phase automatically switches the sound.
- **Sounds** – generated live with the Web Audio API:
  - binaural, monaural or isochronic tones (any beat 1–40 Hz, any carrier 80–500 Hz)
  - pink / brown / white noise beds, or synthesized rain
  - optional 12–18 Hz amplitude modulation on the noise bed (the "rapid modulation" approach that has the best evidence for sustained attention)
- **Evidence** tab – what the peer-reviewed literature actually supports, with citations, and where the app's presets come from.
- Keeps the screen awake, shows lock-screen media controls, counts today's focused minutes.

## Install on a phone
Open the live URL → Share → **Add to Home Screen**. It then runs full-screen and offline.

## Run locally
Any static server, e.g. `python -m http.server 8765` then open http://localhost:8765.

## Files
- `index.html` – the whole app
- `evidence.html` – research summary shown in the Evidence tab
- `sw.js`, `manifest.json`, icons – PWA/offline support

## Disclaimer
Not a medical device. If you have epilepsy, a seizure history, a pacemaker, or are pregnant, check with a clinician before using entrainment audio. Never use while driving.
