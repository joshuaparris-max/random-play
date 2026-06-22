# 🎲 Random Play

A tiny single-page web experiment: when you open it, it picks a **random link** from a list and redirects you there. Handy as a "surprise me" launcher for music tracks, videos, or any set of URLs.

## How it works

- `index.html` fetches `links.json` (a plain array of URLs).
- It picks one at random and redirects the browser to it.
- If `links.json` is missing or empty, it now shows a **friendly fallback page** instead of a broken error.

## Configure your links

Edit `links.json` — just an array of URLs:

```json
[
  "https://example.com/track-1",
  "https://example.com/track-2"
]
```

The included list contains a few placeholder YouTube links — replace them with your own.

## How to run

Because it uses `fetch()`, open it via a local server (not `file://`):

```bash
python -m http.server 8000
# then visit http://localhost:8000
```

Or deploy the folder to any static host (GitHub Pages, Netlify, etc.).

## Status

**Tiny experiment — working.** Intentionally minimal: one HTML file plus a JSON list.
Not intended to grow into a larger app.
