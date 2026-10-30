# ∞ JapMala — Sita Ram

A minimal, single-screen mantra Jap counter with a centered glowing infinity symbol and **Krishna Das's Sita Ram playing through an audio-only SoundCloud widget**.

## Audio

- **Official artist SoundCloud track:** https://soundcloud.com/krishnadasmusic/sita-ram
- **Original YouTube reference:** https://www.youtube.com/watch?v=c3K1BWeIZyo
- The website uses SoundCloud's authorized embedded audio player, rather than extracting an audio track from YouTube.
- **Version caution:** The tracks share the same name and artist and appear to be the same song, but the SoundCloud recording has not been independently matched sample-by-sample to the provided YouTube video.
- No audio file is copied to or hosted by this GitHub repository.

## Features

- Infinity symbol with **only two numbers inside**: completed Jap (left) and Jap target (right).
- Glowing infinity animation, circular and outward-flowing **सीता राम** text while audio plays.
- Audio-only SoundCloud player, with its native Play/Pause controls and looping attempt via the official SoundCloud Widget API.
- Targets: 11, 21, 51, 108, 1008, or a custom amount.
- Automatic **estimated** Jap counting synchronized to SoundCloud's real track playback position, with settings to recalibrate or to manually record exact timings.
- A simple main page with extra timing, manual +1, Undo and Reset controls in ⚙ Settings.
- Local progress saving in the browser. It attempts to preserve saved JapMala progress from earlier versions.

## Counting limitations

SoundCloud's embedded widget exposes track playback position, not the raw audio needed to detect each vocal repetition. Therefore:

1. **Estimated mode** initially uses a provisional, *unverified* 2.2-second interval and starts counting when the artist's track plays. It can count incorrectly during instrumental sections, introductions, and changes in singing speed.
2. **Calibrate interval:** Listen and tap **Mark jap** in Settings at the end of two consecutive complete repetitions. The difference becomes the estimated interval for later counts.
3. **Exact timestamps:** Choose *Exact markers* in Settings and mark the end of each repetition throughout the first full playback. At track completion, the recorded cue points are saved and subsequent loops count at those timestamps.

Seeking forward does not count skipped portions. These timestamps are not pre-verified; for true accuracy, manually validate each repetition against the authorized source audio. Actual playback, embedding permission, automatic replay, and background playback depend on SoundCloud and the browser.

## Run and deploy

Open `index.html` in a browser, or start a local server:

```bash
python -m http.server 8000
```

Then open `http://localhost:8000`.

For GitHub Pages: repository **Settings → Pages → Deploy from a branch → main → / (root) → Save**.

Expected URL: https://abhikakadiya2301.github.io/japmala/
