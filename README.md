# Fred maps

Downloads for [Fred](https://github.com/r-magnus/fred), an offline wilderness
assistant:

- **State map bundles** (release `maps-2026-09`): one per US state, plus DC and
  Puerto Rico. The Fred app downloads a state's bundle when the user picks
  that state.
- **The core download** (release `core-2026-11`, 1.45 GB): the two models and
  the first-aid, survival and outdoor guides every phone needs before Fred can
  answer. The setup wizard downloads it. Files over 100 MB are also published
  in 100 MB pieces, so a dropped connection resumes from the last whole piece.

The files are attached to this repo's
[releases](https://github.com/r-magnus/fred-maps/releases), not stored in git.
`index.json` lists every state's files, and under `core` the core download's,
with sizes, checksums and release asset names.

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

The state bundles hold no medical content. The core download's guides include
first aid, quoted from public-domain US Government manuals and WHO/ICRC *Basic
Emergency Care*; they are reference text for an app, not medical advice. Fred's
own code is private and is not in this repository.
