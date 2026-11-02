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

Any static host works: Cloudflare Pages / Workers static assets, GitHub Pages, Netlify. This repo is published to GitHub Pages by `.github/workflows/pages.yml` on every push to `main`. That needs Settings → Pages → Source set to **GitHub Actions**.

## Versions and builds

- The current version is in [`VERSION`](VERSION) and follows [Semantic Versioning](https://semver.org/). Every release is listed in [`CHANGELOG.md`](CHANGELOG.md) and tagged in git (`v0.9.0`, …).
- On each deploy, the workflow writes `build.json` with the version, commit, build number, commit date and build date. The app shows these at the bottom of the opening page and the editor sidebar, linked to the changelog and to the commit on GitHub.
- Every export records the version and commit that made it: the STL header, the 3MF `Application` metadata, and the first line of `README.txt` in the STL zip. A print can always be traced back to the exact code.

To cut a release:

1. Update `VERSION` (patch for fixes, minor for features, major for breaking changes).
2. Add a section at the top of `CHANGELOG.md`.
3. Commit, then tag it: `git tag -a v0.10.0 -m "v0.10.0"`.
4. Push the commit and the tag: `git push --follow-tags`.

Elevation data attribution: https://github.com/tilezen/joerd/blob/master/docs/attribution.md. Not affiliated with Strava.
