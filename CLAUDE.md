# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## What this is

Source for DirectTrust's GitHub Pages organization landing page, published at
https://directtrust.github.io. It is the entry point that links out to the individual
documentation sites hosted in other repos under the [DirectTrust](https://github.com/DirectTrust)
org — each its own GitHub Pages *project* site, served at `https://directtrust.github.io/<repo-name>/`.

Plain static HTML/CSS. No build step, no framework, no dependencies, no tests.

## Structure

- `index.html` — the entire landing page (single file)
- `assets/style.css` — all styles (DirectTrust brand palette: blue `#004f93`, green `#5cb172`)
- `assets/` — logo and favicon images

## Workflow

Edit `index.html` / `assets/style.css` directly and open the file in a browser to preview —
there's nothing to build or run. Push to `main` and the change is live within a minute or two
(GitHub Pages serves this repo's root directly from the `main` branch).

## Page structure

The page is organized into numbered `.category` sections inside `<main class="wrap">`
(e.g. `Tools`, `Metadata and Payloads Framework`), each containing a `.card-grid` of `.card`
links out to external DirectTrust doc sites.

To add a new published documentation site, add a `.card` link pointing at
`https://directtrust.github.io/<new-repo-name>/` within the relevant category's `.card-grid`.
Cards without an `href` (`.card-disabled`) render as a muted "Coming Soon" placeholder for
work that hasn't been published yet — use this pattern for links to sites not yet live.
