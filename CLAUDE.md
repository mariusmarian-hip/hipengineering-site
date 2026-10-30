# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## What this is

Static website for HIP Engineering, served by GitHub Pages from the `main` branch of `mariusmarian-hip/hipengineering-site` at the custom domain in `CNAME` (`hipengineering.com`). There is no build step, package manager, linter, or test suite — files in the repo root are published as-is on push to `main`.

The site is a one-page company presentation (services, projects, contact) in two languages: Romanian at `index.html` and English at `en/index.html`. Both share `style.css` and have the same structure, so any content change must be made in both files. A language button in the app bar links each page to the other (explicit `index.html` paths so it also works when opened from disk). The only external resources are Roboto and Material Symbols from Google Fonts.

## Working on it

- Preview locally by opening `index.html` in a browser, or serve the folder (e.g. `python -m http.server`) and visit `http://localhost:8000`.
- Do not remove or rename `CNAME` — GitHub Pages uses it to bind the custom domain.
- The repo lives on a Google Shared Drive; `desktop.ini` is a Windows/Drive artifact and should not be committed.

## Conventions

- Plain Material Design 3 look (top app bar, elevated/outlined cards, pill buttons). The owner explicitly wants no animations or transitions and nothing flashy — keep it sober.
- Colors are Material-style tokens on `:root` (`--primary`, `--primary-container`, `--surface`, `--on-surface`, `--outline`, …) with a `prefers-color-scheme: dark` override; add new colors as tokens there rather than hard-coding.
- Icons are Material Symbols ligatures: `<span class="icon">name</span>`.
- Brand: navy `#0f3d5e` + amber `#f5b301`, lightning-bolt logo as inline SVG (also used as a data-URI favicon).
- Projects are described generically — do not name clients on the public site unless the owner confirms it.
