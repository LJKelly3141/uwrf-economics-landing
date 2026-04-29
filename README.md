# UWRF Economics — Landing Page

Editorial landing page for the Economics Program at the University of
Wisconsin–River Falls. Static HTML/CSS/JS — no build step.

## Structure

```
LandingPage/
├── index.html        Main page
├── styles.css        Design system + sections
├── images/           Faculty photos + campus photo
└── README.md
```

## Local preview

```sh
open index.html
```

…or serve from any static server:

```sh
python3 -m http.server 8000
```

## Deployment

Published via GitHub Pages from the `main` branch root. The live URL
resolves at `https://<owner>.github.io/uwrf-economics-landing/`.

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
