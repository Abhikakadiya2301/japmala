# ∞ JapMala — Sita Ram

A minimalist, single-mantra Jap counter with a centered glowing infinity sign and an embedded version of the **exact YouTube video supplied for Krishna Das — Sita Ram**.

**Video:** https://www.youtube.com/watch?v=c3K1BWeIZyo

**Published URL, once GitHub Pages is enabled:** https://abhikakadiya2301.github.io/japmala/

## Features

- A single Sita Ram video embedded using the official YouTube IFrame Player API (no audio downloads or rehosting).
- The infinity loop contains only **numbers**: completed Japs on the left and target Japs on the right.
- A glowing infinity trace, rotating circle of Devanagari words, and floating “सीता राम” characters when playing.
- YouTube Play/Pause, visible video player, and an attempt to restart the video on completion.
- Customizable goals: 11, 21, 51, 108, 1008, or any target up to 1,000,000.
- Saved progress, a manual +1 Jap, Undo, Reset, and audio-synchronization settings.
- Layout optimized for one screen on typical desktop/phone viewports. Very small viewports may need scrolling.

## Auto-count accuracy — please read

**The app does not yet know the exact Sita Ram timestamps in this recording.** It cannot read raw audio or distinguish verses from musical beats through the YouTube IFrame API.

1. **Estimated mode (default):** Counts automatically while the video plays using a *provisional*, **unverified 2.2 seconds/Jap** interval. This may overcount instrumental passages or count incorrectly when chanting speed changes.
2. **Calibrate approximate rhythm:** Tap **Mark jap** at the end of two consecutive complete Sita Ram repetitions. The time between taps becomes the estimated interval for the remainder of playback.
3. **Exact marker mode (higher precision):** Open ⚙ Settings, change Auto-count method to **Exact markers**, play the video from the beginning, and tap **Mark jap** at the completion of **every** repetition for the first full cycle. When the video completes, the timestamps are saved; later loops count automatically at those points. Accuracy is limited by the markings you make.

Seeking forward does not count skipped repetitions. Background playback and embedding may be restricted by YouTube or the browser. Count data stays in this browser's localStorage.

## Run locally

Open `index.html` in a browser or run:

```sh
python -m http.server 8000
```

and visit http://localhost:8000 .

## Deploy

In GitHub: **Settings → Pages → Deploy from a branch → main → / (root) → Save**.

## Licensing and limitations

- The original video remains hosted by YouTube and plays through YouTube's visible, standard embedded player.
- No copyrighted sound recording is copied into this repository.
- YouTube can prohibit embedding or interrupt playback according to the uploader's settings.
- Accurate fully automatic audio-content recognition would require access to an appropriately licensed copy of the recording for analysis and separately verified repetition timestamps.
