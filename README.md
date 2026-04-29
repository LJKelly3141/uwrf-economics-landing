# UWRF Economics — Landing Page

Editorial landing page for the Economics Program at the University of
Wisconsin–River Falls. Static HTML/CSS/JS — no build step.

**Live:** https://ljkelly3141.github.io/uwrf-economics-landing/

## Structure

The site lives in `docs/` so GitHub Pages can serve it from the
`main` branch's `/docs` folder.

```
LandingPage/
├── README.md                            This file
├── .gitignore
└── docs/                                ← GitHub Pages root
    ├── index.html                       Main page (single-file)
    ├── styles.css                       Design tokens + section styles
    └── images/
        ├── kelly.jpg                    Faculty — Logan Kelly (Chair)
        ├── abegaz.jpg                   Faculty — Melaku Abegaz
        ├── bretschneider-fries.jpg      Faculty — Christine Bretschneider-Fries
        ├── dzikpe.jpg                   Faculty — Francis Dzikpe
        ├── campus.png                   Campus break photo (UWRF UMC backdrop)
        └── uwrf-logo.png                UWRF wordmark (not yet placed in markup)
```

## Page sections

1. **Topbar** — sticky navigation, brand mark, primary CTA
2. **Hero** — vertical red rail + giant editorial headline with red-block "&"
3. **Stat strip** — four credibility numbers on a dark band
4. **01 / What is Economics** — dictionary-style definition triplet
5. **02 / Why study Economics** — three numbered rows on a dark field
6. **Campus break** — full-bleed UWRF photo with red caption stripe
7. **03 / Careers** — giant `$115,440` red panel + 8-row career table
8. **04 / Faculty** — four-card grid (grayscale → color on hover)
9. **05 / Final CTA** — red field with mailto-backed form + contact card
10. **Footer** — site map and address

## Local preview

```sh
open docs/index.html
```

…or serve from any static server:

```sh
cd docs && python3 -m http.server 8000
```

## Deployment

Published via GitHub Pages from `main` / `docs/`. Pushing to `main`
triggers a rebuild automatically (typically <60 s).

## Notes for editors

- Section copy lives directly in `index.html`. Headlines and pull-quotes
  use `<em>` for the red italic accent and `<span class="block">` for the
  red-block highlight (used in the hero "&" and the underlined word in
  the final CTA).
- Faculty photos live in `images/` and are rendered grayscale by default,
  blooming to color on hover.
- Theme tokens (colors, fonts, spacing) are CSS variables in the `:root`
  block at the top of `styles.css`. The page is locked to dark mode via
  the `data-theme="dark"` attribute on `<html>` — flip to `light` to
  preview the alternate theme.
