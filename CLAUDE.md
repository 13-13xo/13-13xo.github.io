# I.O.I. (Our Games) — 13-13xo.github.io

Static GitHub Pages site shared by Brooke (`13-13xo`, repo owner, built the site) and Brennan (`13-1V1`, collaborator). Live at https://13-13xo.github.io/. **Pushing to `main` publishes it.**

## Layout
- `index.html` — the whole site (inline CSS/JS/SVG). Two halves in `<main class="stage">`:
  - `section.side.his` — **His Games** (dark steel, lit teal)
  - `section.side.her` — **Her Games** (dark steel, lit amber)
  - Stick (SMAW) welding-seam animation down the middle (steel bead, rod burns down); on phones the weld runs across the top as a strip carrying the title, with His and Her stacked under it.
  - The big title on the weld is **I.O.I.** (iron on iron), chrome that is cool on His side and warm on Hers.
- `his-covers/` — 800x450 card art for Brennan's other games, named by game id (`nowhere-to-hide.webp`, `ibtw.webp`, ...). These cards link out to BEZ Works instead of hosting a build.
- `favicon.svg` — half steel, half bronze heart.
- One folder per game, each a Godot 4.3 single-threaded web export (`index.html/.js/.wasm/.pck`, icons):
  - `shoot-the-shit/` — Brooke's version (Her Games, inline SVG card art)
  - `his-shoot-the-shit/` — Brennan's 1.0.0 (His Games, `card.webp` art)

## Adding a game
1. Add a folder with the Godot 4.3 single-threaded web export.
2. In the game's `index.html`, add `<a id="back" href="../">&larr; workshop</a>` linking back to the site.
3. Add an `<a class="plate" href="folder/">` card inside `.games` of the right half: a 16:9 `.thumb` (800x450 image or SVG), `<strong>` title, a `<span>` blurb, and `<span class="size">` download size.

### Cards that link out (BEZ Works games)
Same `<a class="plate">` shape, but `href` is an absolute BEZ Works URL with `rel="noopener"`, the image has `alt=""` and `loading="lazy"` (the title and blurb already name the link), and the `size` line says where it goes, e.g. "Windows · Mac · opens BEZ Works". Games that play in a browser use `.../BEZ-Works/play/<id>/`; download-only ones use `.../BEZ-Works/#<id>`. Cover art: crop to 16:9, 800x450 webp, into `his-covers/`.

## How the page behaves
- 820px and under is the phone layout: the weld strip and title sit at the top, His and Her stack under it. Wider is side by side.
- The weld intro runs about 8 seconds and a click or key press skips it. Reduced-motion skips it entirely.
- Fonts are Impact-style system fonts, so the headings look different on Android and Linux.

Brennan's desktop/Android downloads for Shoot The Shit live on his other site: https://13-1v1.github.io/BEZ-Works/#shoot-the-shit (separate repo/session).

## Rules
- Brooke owns the repo and doesn't know GitHub well. Never rewrite her design, her game, or her history without Brennan's clear OK.
- Never force-push.
- Ask Brennan before pushing — pushing goes live.
- Prefer changes through a branch + PR (as with PR #1) unless Brennan says otherwise.
