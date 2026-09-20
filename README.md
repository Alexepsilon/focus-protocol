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

## What the research says (short version)
Full write-up with ~75 citations is in the app's **Evidence** tab.

| Finding | Confidence |
|---|---|
| For plain reading, silence is at least as good as any sound. Sound's real job is masking speech and intermittent noise. | strong |
| 16 Hz amplitude-modulated noise/music is the best-supported "focus sound" for sustained attention (biggest effect in high-ADHD-trait listeners; vendor-affiliated research). | moderate |
| Binaural beats: pooled medium effect, but the best-powered replication of the beta-band attention claim is null. Beta 15-20 Hz has weak positive memory-encoding data; theta impairs recall. | weak |
| 40 Hz gamma: mixed for attention, and the dementia research does not transfer to students. | weak |
| Brown noise has no specific evidence over pink or white. | null |
| Nature sounds before a block reduce stress (g = -0.60) and modestly restore attention. | strong / moderate |
| Retrieval practice (g = 0.5-0.6 vs re-reading) and spacing matter far more than any sound. Every protocol ends each block with a recall phase. | strong |
| Block length does not change learning; fixed blocks just stop you over-running. 90-min "ultradian" cycles have no physiological support. | moderate |
| Continuous pink noise during sleep does not improve memory. The EEG-timed version does, and a phone can't do it. | null |
| Keep it quiet: benefits appear around 45 dB; WHO budget is 80 dB for 40 h/week. | strong |

## Protocols
- **Deep work** 3 prime, then (45 focus / 5 recall / 10 break) x 3
- **Pomodoro** (22 focus / 3 recall / 5 break) x 4
- **Memorise** (20 study with beta-16 / 10 recall / 5 break) x 3
- **Exam sprint** 3 prime, then 90 min plain noise
- **Monroe wind-down** 20 min, 4 Hz on 100 Hz over pink noise (relaxation only)
- **Custom**

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
