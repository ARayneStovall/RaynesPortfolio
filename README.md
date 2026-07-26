# Abby Rayne Stovall — Portfolio

Personal portfolio site, live at [araynestovall.github.io/RaynesPortfolio](https://araynestovall.github.io/RaynesPortfolio/).

## Stack

Single-file static site. No build step, no framework, no dependencies.

- `index.html` — everything: markup, `<style>`, and `<script>` all live in this one file
- Fonts loaded from Google Fonts (Newsreader, IBM Plex Sans, IBM Plex Mono)
- Deployed via GitHub Pages, auto-builds from `main`

## Structure

```
index.html       all markup, CSS, and JS
media/           images, video, résumé PDF
robots.txt
sitemap.xml
```

Theming is driven by CSS custom properties in `:root`, with a `@media (prefers-color-scheme: dark)` block overriding the same variables for dark mode. The site switches automatically based on the visitor's OS setting — there's no manual toggle.

## Editing

Open `index.html` in a browser to preview locally, no server needed. Since it's a single file, most changes are just editing markup or the `:root`/dark-mode variable blocks directly.

A few things worth knowing before making changes:

- **Check both color schemes.** Any CSS change should be checked in both light and dark mode (e.g. via browser devtools' rendering emulation), since they share selectors but diverge on custom-property values.
- **`media/og-image.jpg` and `media/gaugecalc-preview.jpg` are static screenshots, not CSS-driven.** If the color palette or the live gaugeCalc app changes, these won't update on their own and need to be regenerated manually.
- **Media sizing.** Images and videos use explicit `width`/`height` attributes to prevent layout shift, paired with `height:auto` in CSS. Dropping the CSS `height:auto` while keeping the HTML attributes will distort the image.

## Deployment

Push to `main` and GitHub Pages rebuilds automatically. No manual deploy step.
