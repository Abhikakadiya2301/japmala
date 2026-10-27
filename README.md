# ∞ JapMala — Sita Ram Jap Counter

JapMala is a minimalist, static website centered around a single Sita Ram chant.

**Selected recording:** https://www.youtube.com/watch?v=c3K1BWeIZyo

## What's included

- Embedded YouTube playback of the selected recording (no downloaded or redistributed audio).
- Continuous video looping when YouTube embedding and playback are permitted.
- Glowing animated infinity sign: **only numbers** inside the loops — completed Jap on the left, target on the right.
- Animated outward-flowing `सीता राम` text and rotating Devanagari ring while playing.
- Custom Jap targets (11, 21, 51, 108, 1008, or a custom number), 108 beads and local progress.
- Manually count or undo individual repetitions.
- Two ways to synchronize automatic counting with the chant's **video playback time**:
  - **Automatic rhythm — estimated:** Jap counting starts on playback using a provisional **2.2 seconds per Jap** interval. This is **not measured from the actual singing** and can count during instrumental passages. In Settings, adjust the seconds-per-Jap value, or click *Mark jap* at the end of two consecutive full repetitions to calibrate the estimate for later repetitions. Mark taps used for rhythm calibration do not themselves add Jap.
  - **Exact timestamps — learn once:** Set sync mode to *Exact timestamps*, play the full song and tap *Mark completed jap* after each complete repetition. When the video finishes, the saved timestamps replay on following loops, adding one Jap at each marked completion.

## Counting accuracy

**YouTube's embedded player API supplies video time, not raw audio.** The app cannot recognize each mantra directly from its sound and cannot automatically distinguish musical beats from repetitions. The default 2.2-second interval is only a starting guess, not verified from the recording. Rhythm counting is an estimate for uniform pacing and may drift, especially during instrumental introductions or musical changes. Exact mode is accurate relative to the timestamps you mark. Playback seeking does not count skipped portions. A 1-second discontinuity threshold helps prevent false counts on a seek.

On first listen using exact mode, pressing the mark button also increments the count. Future loops use the saved markers instead; avoid marking again after learning is complete. You can correct mistakes with Undo. Sync settings and Jap totals are stored in browser localStorage; they do not transfer between devices.

YouTube embedding availability, advertisements, third-party cookie policies, playback restrictions, and mobile background behavior depend on YouTube and the visitor's browser. If the video is blocked from embedding, follow the YouTube link.

## Run and deploy

Run the static `index.html` through a local web server, such as `python -m http.server 8000` and visit http://localhost:8000 .

To publish: GitHub repository **Settings → Pages → Deploy from a branch → main → / (root) → Save**.

Expected website: https://abhikakadiya2301.github.io/japmala/

No build system, bundled audio, API keys, or paid hosting required.
