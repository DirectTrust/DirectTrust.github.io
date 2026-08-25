# DirectTrust.github.io

Source for the DirectTrust organization's GitHub Pages landing page, published at
[https://directtrust.github.io](https://directtrust.github.io).

This is the entry point for DirectTrust's open technical resources — a landing page that
links out to the individual documentation sites hosted in other repos under the
[DirectTrust](https://github.com/DirectTrust) org (each its own GitHub Pages *project* site,
served at `https://directtrust.github.io/<repo-name>/`).

## Structure

Plain static HTML/CSS — no build step, no framework, no dependencies.

- `index.html` — the landing page
- `assets/style.css` — styles (DirectTrust brand palette: blue `#004f93`, green `#5cb172`)
- `assets/` — logo and favicon images

## Editing

Edit `index.html` / `assets/style.css` directly and open the file in a browser to preview —
there's nothing to build. Push to `main` and the change is live within a minute or two
(GitHub Pages serves this repo's root directly from the `main` branch).

## Adding a new documentation link

Each category on the page (`Tools`, `Metadata and Payloads Framework`, ...) is a `.card-grid`
of `.card` links in `index.html`. To add a new published site, add a card pointing at
`https://directtrust.github.io/<new-repo-name>/`. Cards without an `href` (`.card-disabled`)
render as a muted "coming soon" placeholder for work that hasn't been published yet.
