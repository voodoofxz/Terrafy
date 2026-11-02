# Terrafy

**Your route. Made real.**

**Try it:** https://voodoofxz.github.io/Terrafy/

Brand: the official logos are `brand/terrafy-logo-light.webp` and `brand/terrafy-logo-dark.webp`, used unmodified. The app shows the one that matches the light/dark mode. The UI palette is sampled from them: logo backgrounds `#fcfbfc` and `#020914`, sky `#0356e7` → `#0fd5f2`, wordmark blue `#017ffd` → mint `#08e3ab`.

A free, single-page web app that turns Strava rides and routes (GPX exports) into 3D-printable topographic relief maps.

- Drop one or more GPX files (Strava: activity or route → Export GPX). Files never leave the browser.
- Terrain comes from the free [Terrain Tiles on AWS](https://registry.opendata.aws/terrain-tiles/) (Mapzen/Tilezen Terrarium, up to zoom 14).
- Color the terrain in height bands; the page lists the Z heights for filament swaps.
- Drag across the elevation profile to mark favorite segments, which print raised in their own color.
- Export a multi-part 3MF (terrain, route, and one part per segment color), a single STL, or a zip of STLs, one per color.

## Run locally

It's one static file. Serve the folder with any static server and open it, for example:

```bash
npx serve .
```

## Host for free

Any static host works: Cloudflare Pages / Workers static assets, GitHub Pages, Netlify. This repo is published with GitHub Pages from the `main` branch root; `.nojekyll` makes Pages serve the files as-is.

Elevation data attribution: https://github.com/tilezen/joerd/blob/master/docs/attribution.md. Not affiliated with Strava.
