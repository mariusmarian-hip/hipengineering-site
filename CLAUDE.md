# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## What this is

Static website for HIP Engineering, served by GitHub Pages from the `main` branch of `mariusmarian-hip/hipengineering-site` at the custom domain in `CNAME` (`hipengineering.com`). There is no build step, package manager, linter, or test suite — files in the repo root are published as-is on push to `main`.

Currently the site is a single work-in-progress landing page (`index.html`) with inline CSS and a one-line inline script; there are no external assets or dependencies.

## Working on it

- Preview locally by opening `index.html` in a browser, or serve the folder (e.g. `python -m http.server`) and visit `http://localhost:8000`.
- Do not remove or rename `CNAME` — GitHub Pages uses it to bind the custom domain.
- The repo lives on a Google Shared Drive; `desktop.ini` is a Windows/Drive artifact and should not be committed.

## Conventions in `index.html`

- Content is primarily Romanian (`<html lang="ro">`), with a secondary English line.
- Colors are CSS custom properties on `:root` (`--bg`, `--fg`, `--muted`, `--accent`, `--brand`, `--line`) with a `prefers-color-scheme: dark` override; add new colors as tokens there rather than hard-coding.
- Brand: navy `#0f3d5e` + amber `#f5b301`, lightning-bolt logo as inline SVG (also used as a data-URI favicon).
- The page has `<meta name="robots" content="noindex">` while under construction — remove it when the real site launches.
- Animations respect `prefers-reduced-motion`.
