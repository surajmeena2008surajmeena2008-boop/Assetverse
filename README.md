<p align="center">
  <img src="assets/icon.svg" width="120" alt="AssetVerse icon">
</p>

<h1 align="center">AssetVerse</h1>

<p align="center">
  Every icon, logo, sticker, emoji, symbol &amp; font in one studio.<br>
  Customise colour, texture and size, then export as <b>SVG</b> or <b>PNG</b>.
</p>

## Features

- **Icons** (Lucide + Iconify sets), **brand logos** (Simple Icons, original colours), **stickers**, **emojis**, **symbols** and **Google Fonts**
- Live customiser: colour, texture, size, bold/italic, font
- 12 UI themes (glass, liquid glass, neumorphic, clay and more)
- Export to SVG or PNG, copy font CSS
- Single static file, no build step

## Run it

It loads libraries and icon data from CDNs, so **an internet connection is required**.

```bash
# any static server works
python3 -m http.server 8080
# open http://localhost:8080
```

Opening `index.html` directly also works in most browsers.

## Deploy on GitHub Pages

1. Push this repo to GitHub.
2. Go to **Settings → Pages → Source: GitHub Actions**.
3. The workflow in `.github/workflows/pages.yml` deploys on every push to `main`.

## Install as an app

The app is a PWA, but installing only works over **HTTPS** (for example your GitHub Pages link), not from a downloaded file.

- **Android / Chrome:** open the live link → menu (⋮) → **Install app**
- **iPhone / Safari:** Share → **Add to Home Screen**
- **Desktop Chrome / Edge:** install icon in the address bar

If you installed it earlier and still see a letter instead of the icon, remove the old shortcut and install again.

## Network dependencies

| Used for | Source |
|---|---|
| React, Framer Motion, Lucide, Simple Icons | esm.sh |
| Tailwind (browser build) | cdn.jsdelivr.net |
| Emoji data | cdn.jsdelivr.net (emojibase-data) |
| Online icon sets & search | api.iconify.design |
| Font list | api.fontsource.org |
| Fonts | fonts.googleapis.com |

Requests use a 12 s timeout with automatic retries, and the UI shows a **Retry** button if a library fails to load.

## License

MIT
