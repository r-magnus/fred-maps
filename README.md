# Fred maps

Offline map bundles for [Fred](https://github.com/r-magnus/fred), an offline
wilderness assistant: one bundle per US state, plus DC and Puerto Rico. The
Fred app downloads a state's bundle when the user picks that state.

The files are attached to this repo's
[releases](https://github.com/r-magnus/fred-maps/releases), not stored in git.
`index.json` lists every state's files, sizes, SHA-256 checksums and release
asset names.

## What a bundle holds

| File | What it is |
|---|---|
| `map-<ST>-z14.pmtiles` | Basemap to zoom 14: roads, trails, water, land cover |
| `contours-<ST>.pmtiles` | Contour lines (200 m / 100 m / 40 m by zoom) |
| `coverage-<ST>-voice.bin` | Where each mobile carrier reports voice coverage (for 911), per carrier |
| `packs/state-<ST>-flora-fauna/` | Plant and animal reference text with search vectors (not in DC and PR) |
| `bundle.json` in the index | Sources, build date, checksums |

Sizes run from 21 MB (Hawaii) to 1.3 GB (Alaska); 15.7 GB in all.

## Licences

This data comes from several sources, each under its own terms. See
[NOTICE.md](NOTICE.md) for the licences and the credits that must be shown
alongside it. In short: the basemap is OpenStreetMap data under the ODbL;
everything else is public domain or open data with attribution.

Nothing here is medical content. Fred's own code is private and is not in this
repository.
