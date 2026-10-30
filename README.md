# ∞ JapMala — Sita Ram

JapMala is a minimal, saffron-themed mantra Jap counter with a centered glowing infinity symbol and the **Krishna Das Sita Ram YouTube video** displayed below it.

**Original video:** https://www.youtube.com/watch?v=c3K1BWeIZyo

**Website:** https://abhikakadiya2301.github.io/japmala/

## Features

- The original YouTube video is embedded with the YouTube IFrame Player API, including its native playback controls. The video remains visible; no audio is downloaded, extracted, or rehosted.
- The center infinity loops show only numbers: completed Japs on the left, target Japs on the right.
- Minimal saffron and sandalwood-ivory palette with a glowing infinity and floating **सीता राम** text during playback.
- Customizable targets: 11, 21, 51, 108, 1008, or a custom goal.
- Automatic estimated counts based on playback position (see accuracy warning below).
- Settings (⚙) include manual +1, Mark jap, Undo, Reset and synchronization options, keeping the main screen uncluttered.
- Per-browser local progress persistence.

## Counting accuracy

The YouTube IFrame API exposes playback position but **does not provide audio-content recognition**.

- **Estimated mode (default):** Uses an initial, unverified **2.2 seconds per Jap** assumption. It is not aligned to verified chant repetitions and can overcount musical passages or be incorrect when the tune changes.
- **Calibrated estimate:** In Settings, press **Mark jap** at the end of two consecutive complete chants to set an estimated interval.
- **Exact markers:** In Settings choose *Exact markers*, then play the song from the beginning and mark the end of every actual Sita Ram repetition during the first full play. Saved timestamps are then reused on following loops. Accuracy depends on your manual timing.

Forward seeks do not add skipped Japs. YouTube embedding, looping, ads and background behavior are subject to YouTube and the browser.

## Local setup and deployment

Open `index.html` in your browser, or run:

```sh
python -m http.server 8000
```

Then visit http://localhost:8000.

For GitHub Pages: **Settings → Pages → Deploy from a branch → main → / (root) → Save**.
