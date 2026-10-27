# 🪷 JapMala — Digital Mantra Counter

A lightweight, mobile-friendly chanting website for **any mantra** with configurable repetition goals.

## Features
- Sita Ram, Om Namah Shivaya, Shri Ram Jai Ram, Gayatri Mantra, Swaminarayan, and custom mantra text.
- Targets: 11, 21, 51, 108, 1008 or a custom number.
- Manual **+1 Jap** button and Undo.
- Automatic counting **once per completed audio file** and seamless looping attempts.
- 108-bead progress display and completed mala count.
- Saved counts by mantra using browser localStorage.
- No build step, account, analytics, or server required.

## Run
Open `index.html` in a modern browser, or serve it locally using:

```bash
python -m http.server 8000
```

Then open `http://localhost:8000`.

## Publish with GitHub Pages
1. Go to this repository's **Settings → Pages**.
2. Under *Build and deployment*, select **Deploy from a branch**.
3. Select **main**, folder **/(root)**, and Save.
4. The public website should become available at **https://abhikakadiya2301.github.io/japmala/** once GitHub deploys it.

## Important: accurate chanting counts
The application cannot automatically recognize the number of words/mantras inside arbitrary songs. **Automatic count = 1 whenever the selected audio clip reaches its end**. For accurate auto-counting, supply an audio recording containing exactly **one** full mantra repetition (one Jap). The site replays it after each completion. If you use a full devotional track with many repetitions, use manual counting instead.

Upload your own or a properly licensed audio clip through the web page. It remains locally in your browser, and you must reselect it after refreshing. No copyrighted audio is bundled with this repository.

Counters are browser-local and should not be treated as verified across different devices; clearing browser data may erase them. Some browsers may restrict background playback.

## Tech stack
Single static HTML/CSS/JavaScript file, with no dependencies.
