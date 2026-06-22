# 🎲 random-play — Serendipity Player

A tiny "surprise me" launcher. Pick a vibe (Music, Focus, Worship/Reflection, Kids/Family,
Fun), hit **Surprise me**, and get one random pick — shown on a landing card so *you* decide
whether to open it. No auto-redirect, no tracking, nothing sent anywhere.

## Features

- Landing page with category filters (no surprise redirect-on-load).
- **Surprise me** picks a random item from the selected category (or All).
- **Open in new tab**, **Copy link**, and **Roll again** actions.
- Graceful fallback if `links.json` is missing or empty.
- Fully static — one `index.html` + `links.json`.

## Add your own links

Edit [`links.json`](links.json). Each category has an `id`, `label`, `emoji`, and `items`:

```json
{ "id": "music", "label": "Music", "emoji": "🎵",
  "items": [ { "title": "Lofi beats", "url": "https://..." } ] }
```

## Run

It uses `fetch()`, so serve it over HTTP (not `file://`):

```bash
python -m http.server 8000   # then open http://localhost:8000
```

Or open the live GitHub Pages build.

## Status

See [STATUS.md](STATUS.md). **Working MVP** — categories, random pick, copy/open, fallback.
