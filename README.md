# Terrafy

**Your route. Made real.**

Brand: `logo.svg` is the vector "T" mark used in the app header and as the favicon, and `brand/terrafy-logo.webp` is the full original logo. The UI palette follows the logo's sky-blue gradient (`#0b5ec5` → `#2aa7dc`) and forest greens (`#1e7f5c`, `#0f3a2b`), with a light/dark toggle.

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

Any static host works: Cloudflare Pages / Workers static assets, GitHub Pages, Netlify.

Elevation data attribution: https://github.com/tilezen/joerd/blob/master/docs/attribution.md. Not affiliated with Strava.
