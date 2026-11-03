# Changelog

All notable changes to Terrafy. Versions follow [Semantic Versioning](https://semver.org/). Terrafy stays on 0.x during beta testing, and 1.0.0 will be the public launch. Each version has a matching git tag (`v0.9.0`, …).

## [0.11.0] - 2026-11-02
### Added
- Paste-a-Strava-link shortcut on the opening page and in the editor. Paste a ride (`strava.com/activities/…`) or route (`strava.com/routes/…`) link to get a one-tap button to Strava's own GPX export. Strava downloads the file in your browser (signed in as you), and the drop box pulses to show where it goes. Pasting a Strava link anywhere on the page fills in the box. Share links (`strava.app.link`) and other links get a hint explaining what to paste instead.

## [0.10.0] - 2026-11-02
### Added
- "Enhance... enhance... enhance..." loading screen (with apologies to *Super Troopers*): a zooming reticle with CRT scanlines while the 3D terrain builds. The first build after adding a ride plays all three steps, and later rebuilds only show it if loading is slow.
- Settings sections fold open and closed by tapping their heading.
### Changed
- Simpler phone layout: a compact header, then the 3D map and elevation profile, then the settings with only "Add rides" and "Export" open. The page is now under two screens tall.
- On narrow screens the 3D view pulls back so the whole map fits, and the profile hint is shorter.

## [0.9.0] - 2026-11-02
### Added
- Version and build info: the app shows its version, build number, commit and build date on the opening page and in the editor, linked to this changelog and the commit on GitHub.
- Every export records the Terrafy version and commit that made it: STL header, 3MF metadata and the print notes in the STL zip.
- GitHub Actions deploy workflow that stamps `build.json` (version, commit, build number, dates) into each GitHub Pages deploy.
- `VERSION` file and this changelog.

## [0.8.0] - 2026-11-02
### Added
- Segment end markers in eight shapes: star, heart, lightning, flag, peak, crown, gem, dot. They print as solid shapes and also show on the elevation profile.
- Water color: sea and lakes at 0 m get their own color, set for each theme. They print as the first layers, and land starts 0.6 mm higher.
- Label fonts: bold sans, classic, serif, book, mono.
- Optional printable outline around the label text, with its own color and width.

## [0.7.0] - 2026-11-02
### Added
- Multi-ride totals on the label: ride count, total distance, total climbing, date range and total ride time. Highlight tracks are not counted.
- Rainbow and Unicorn color themes.
### Fixed
- The elevation profile line stays visible when the route color matches the background.

## [0.6.0] - 2026-11-02
### Added
- Opening page with the logo, tagline and a single "Add your ride" box. Loading a ride opens the editor.
- Raised star markers at both ends of favorite segments.

## [0.5.1] - 2026-11-02
### Added
- Published on GitHub Pages at https://voodoofxz.github.io/Terrafy/.

## [0.5.0] - 2026-11-02
### Added
- Four color themes: Terrafy, Autumn Ridge, Ultraviolet, Rose & Sage.

## [0.4.0] - 2026-11-02
### Added
- Official Terrafy logos for light and dark mode, the brand color palette, and a light/dark toggle.

## [0.3.0] - 2026-11-02
### Changed
- Renamed from "Ride Relief" to **Terrafy**, with the tagline "Your route. Made real."

## [0.2.0] - 2026-11-02
### Added
- Easier segment marking: step-by-step instructions, an on-chart hint, a pop-up Add box above the selection, and typed start/end distances.

## [0.1.0] - 2026-11-02
### Added
- First version: load a GPX, get terrain from AWS Terrain Tiles, build a raised route, set color bands with filament-swap heights, drag on the elevation profile to mark segments, add a ride-details label plate and complementary color themes, and export STL, 3MF or a zip of STLs, one per color.

[0.11.0]: https://github.com/voodoofxz/Terrafy/compare/v0.10.0...v0.11.0
[0.10.0]: https://github.com/voodoofxz/Terrafy/compare/v0.9.0...v0.10.0
[0.9.0]: https://github.com/voodoofxz/Terrafy/compare/v0.8.0...v0.9.0
[0.8.0]: https://github.com/voodoofxz/Terrafy/compare/v0.7.0...v0.8.0
[0.7.0]: https://github.com/voodoofxz/Terrafy/compare/v0.6.0...v0.7.0
[0.6.0]: https://github.com/voodoofxz/Terrafy/compare/v0.5.1...v0.6.0
[0.5.1]: https://github.com/voodoofxz/Terrafy/compare/v0.5.0...v0.5.1
[0.5.0]: https://github.com/voodoofxz/Terrafy/compare/v0.4.0...v0.5.0
[0.4.0]: https://github.com/voodoofxz/Terrafy/compare/v0.3.0...v0.4.0
[0.3.0]: https://github.com/voodoofxz/Terrafy/compare/v0.2.0...v0.3.0
[0.2.0]: https://github.com/voodoofxz/Terrafy/compare/v0.1.0...v0.2.0
[0.1.0]: https://github.com/voodoofxz/Terrafy/releases/tag/v0.1.0
