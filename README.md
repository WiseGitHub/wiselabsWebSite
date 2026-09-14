# wiselabsWebSite

The **WiseLabs public website** — a static, single-page catalog of the sound-design and
music output (DAW content, sample/loop packs, synths, effects), plus a couple of small
in-browser **Production tools** and a hidden interactive easter egg. Deployed via GitHub
Pages on a custom domain.

## What it is

Hand-written static HTML/CSS/JS — no framework, no build step. One long `index.html`
carries the whole site (hero, catalog sections, tools, footer) with all CSS and JS inline
and a runtime **accent-hue** slider that re-themes the page live. `index-standalone.html`
is a self-contained variant.

## Layout

| Path | Purpose |
|---|---|
| `index.html` | The site (all sections + inline CSS/JS) |
| `index-standalone.html` | Self-contained variant |
| `404.html` | Not-found page |
| `_egg/` | Hidden interactive pieces (e.g. `looper.html`, loaded on a knock sequence) |
| `assets/` | Images / artwork (`.webp`, og-image, favicons) |
| `loops/` | Audio previews |
| `CNAME`, `.nojekyll` | GitHub Pages custom domain + "serve files as-is" flag |

The **Production tools** (`#tools` section in `index.html`) are self-contained in-browser
utilities — an FPS/FPB optimizer and a random name generator — built from the site's own
CSS tokens so they follow the accent hue.

## Build, run & deploy

No build. To preview locally, serve the folder statically, e.g.:

```bash
cd C:/dev/wiselabsWebSite && python -m http.server 4173
```

then open `http://localhost:4173/index.html`. Deploy is GitHub Pages: pushing to the
published branch updates the live site (custom domain via `CNAME`, Jekyll disabled via
`.nojekyll`).

## Status

Active. ~13 commits. `attempt.txt` is a scratch note and can be removed when convenient.
