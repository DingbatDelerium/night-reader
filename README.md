# Night-Reader

A single-file PWA: a browsable lexicon ("Harmonic Resonance Lexicon") for
reading in the hours between evening and dawn.

## Running it

No build step, no dependencies. Just serve the folder and open it:

```bash
python3 -m http.server 8000
```

Then visit `http://localhost:8000/index.html`.

It also works as an installable PWA (add to home screen) and offline once
loaded once, via the included service worker.

## Files

- `index.html` — the entire app: markup, styles, and the lexicon data,
  all in one file.
- `manifest.json` — PWA manifest (name, icons, theme colors).
- `sw.js` — service worker that caches the app shell for offline use.
- `icon-192.png`, `icon-512.png` — app icons.

## Using the app

- **Tabs** (All / Bridge / Field / Scroll) filter entries by layer.
- **Search** filters by title, body, or definition text.
- **Ember button** (☾ / ☽) on each entry saves it to your personal
  "Pocket Embers" list, stored in your browser's local storage.
- **Random** opens a "Spotlight" view showing one entry at a time from
  the current filtered set.

See `CLAUDE.md` for the lexicon's internal structure and the project's
coding/continuity conventions.
