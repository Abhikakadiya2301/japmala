# ∞ JapMala — Sita Ram Jap

A minimalist, single-screen, **audio-only** Sita Ram Jap counter hosted with GitHub Pages.

Website (once GitHub Pages is enabled): https://abhikakadiya2301.github.io/japmala/

## What it does

- The large, glowing ∞ symbol shows **only numbers** inside the two loops: completed Jap (left), target (right).
- Animated circular and floating **सीता राम** text runs while chanting.
- Press **Play chant** to hear a browser-generated spoken **Sita Ram** in a continuous series.
- **Automatic Jap counting** increments once at the completion of **each spoken phrase**, based on the browser's speech-synthesis completion event — not a guessed music tempo.
- Choose targets of 11, 21, 51, 108, 1008 or a custom goal under ⚙ Settings.
- Pause / resume, manually add Jap, undo, adjust voice speed, optionally enable/disable an original ambient drone.
- Saves the counter on this device in localStorage (attempts to migrate earlier JapMala progress).
- No video, no embedded YouTube player, no third-party scripts and no audio files in the repository.

## Important: this is **not** the linked YouTube song

The original reference was https://www.youtube.com/watch?v=c3K1BWeIZyo .

**Its audio is not downloaded, extracted, embedded or hosted.** The current audio-only version instead uses the browser's speech-synthesis voice (Devanagari if a Hindi voice is available; otherwise “Seeta Ram” in a fallback voice). The optional low-volume ambient sound is an original oscillator-based background, **not** the original music.

If you want that **exact** song without video, supply a properly licensed standalone audio file you have permission to host. That is a separate integration. A long recording containing many mantra repetitions will also need validated repetition timings or segmented audio for accurate Jap counts.

## How to run

Open `index.html` in Chrome, Edge or Safari, or run:

```sh
python -m http.server 8000
```

Then visit http://localhost:8000 .

## Publish with GitHub Pages

Under **Settings → Pages**, choose **Deploy from a branch → main → / (root) → Save**.

## Notes on accuracy and browser support

- **A Jap is added only after the browser announces completion of one synthesis utterance** containing one Sita Ram repetition. This is much more defensible than estimating completions from a musical beat.
- Speech voices, timing and quality depend on the device and installed browser voices. The fallback voice may not sound like traditional singing.
- Browser backgrounding, audio focus, power saving or voice-service errors may interrupt continuous chanting. The app never counts an utterance that its playback loop did not complete in active mode.
- Counts and settings are per-browser and can be lost if site storage is cleared.
- Settings include manual corrections and a reset option.
