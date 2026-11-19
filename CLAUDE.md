# Our Games — 13-13xo.github.io

Static GitHub Pages site shared by Brooke (`13-13xo`, repo owner, built the site) and Brennan (`13-1V1`, collaborator). Live at https://13-13xo.github.io/. **Pushing to `main` publishes it.**

## Layout
- `index.html` — the whole site (inline CSS/JS/SVG). Two halves in `<main class="stage">`:
  - `section.side.his` — **His Games** (brushed steel)
  - `section.side.her` — **Her Games** (warm copper)
  - TIG welding-seam animation down the middle; on phones a His/Her toggle tab switches sides.
- `favicon.svg` — half steel, half bronze heart.
- One folder per game, each a Godot 4.3 single-threaded web export (`index.html/.js/.wasm/.pck`, icons):
  - `shoot-the-shit/` — Brooke's version (Her Games, inline SVG card art)
  - `his-shoot-the-shit/` — Brennan's 1.0.0 (His Games, `card.webp` art)

## Adding a game
1. Add a folder with the Godot 4.3 single-threaded web export.
2. In the game's `index.html`, add `<a id="back" href="../">&larr; workshop</a>` linking back to the site.
3. Add an `<a class="plate" href="folder/">` card inside `.games` of the right half: a 16:9 `.thumb` (800x450 image or SVG), `<strong>` title, a `<span>` blurb, and `<span class="size">` download size.

Brennan's desktop/Android downloads for Shoot The Shit live on his other site: https://13-1v1.github.io/BEZ-Works/#shoot-the-shit (separate repo/session).

## Rules
- Brooke owns the repo and doesn't know GitHub well. Never rewrite her design, her game, or her history without Brennan's clear OK.
- Never force-push.
- Ask Brennan before pushing — pushing goes live.
- Prefer changes through a branch + PR (as with PR #1) unless Brennan says otherwise.
