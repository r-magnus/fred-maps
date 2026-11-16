# Sources, licences and required credits

Checked 2026-09-28. Each component keeps its source's licence; nothing here
relicenses anyone's data.

## Basemap: `map-<ST>-z14.pmtiles`, and the regional and overview maps

- **Source:** Protomaps daily planet build (https://build.protomaps.com), cut to
  each state's bounding box.
- **Licence:** Open Database License 1.0 (ODbL), as a Produced Work of
  OpenStreetMap. https://opendatacommons.org/licenses/odbl/1-0/
- **Required credit, shown with the map:** "© OpenStreetMap contributors"
  (https://www.openstreetmap.org/copyright).
- These extracts are offered under the same licence.
- The same applies to the regional downloads (`map-<ST>-<region>.pmtiles`,
  `map-<ST>-overview.pmtiles`) and the nationwide `map-US-overview.pmtiles`,
  which are further cuts of Protomaps builds.

## Contours: `contours-<ST>.pmtiles` and `contours-<ST>-<region>.pmtiles`

Contour lines computed from Mapterhorn terrain tiles
(https://mapterhorn.com, source list https://download.mapterhorn.com/attribution.json).
Only the derived lines are distributed, not the elevation tiles.

- **United States:** USGS 3D Elevation Program (1 m and 1/3 arc-second DEMs).
  Public domain (US Government work). Credit: "U.S. Geological Survey".
- **Canada (state boxes reaching over the border):** Canada DTM, Natural
  Resources Canada, under the Open Government Licence – Canada
  (https://open.canada.ca/en/open-government-licence-canada). Credit:
  "Contains information licensed under the Open Government Licence – Canada.
  Natural Resources Canada."
- **Mexico and anywhere else outside those:** Copernicus GLO-30 DEM, under the
  Copernicus full, free and open licence. Required notice for derived
  products: "produced using Copernicus WorldDEM-30 © DLR e.V. 2010-2014 and ©
  Airbus Defence and Space GmbH 2014-2018 provided under COPERNICUS by the
  European Union and ESA; all rights reserved".
- Credit for the tiles: "Terrain: Mapterhorn".

## Region outlines: `regions-<ST>.json`

- **Source:** US Census Bureau cartographic boundary files (counties, 1:500k,
  https://www2.census.gov/geo/tiger/GENZ2023/shp/), counties grouped into
  regions and simplified.
- **Terms:** public domain (US Government work). Credit: "US Census Bureau".

## Coverage: `coverage-<ST>-voice.bin`

- **Source:** FCC Broadband Data Collection, mobile voice availability filed by
  each carrier (https://broadbandmap.fcc.gov), repacked by carrier.
- **Terms:** public FCC data; the FCC asks for attribution. Credit: "Coverage:
  FCC National Broadband Map". No Broadband Serviceable Location Fabric data
  (licensed by CostQuest) is used or included.
- Carrier-reported models, not measurements. They are least reliable in the
  canyons and forests Fred is meant for.

## Plants and animals: `packs/state-<ST>-flora-fauna/`

- **Text:** USDA Forest Service Fire Effects Information System (FEIS) Species
  Reviews (https://research.fs.usda.gov/feis). USDA web content "is considered
  public information and may be distributed or copied"; credit requested.
  Credit: "Fire Effects Information System, USDA Forest Service".
- **Images:** none. Photo credit lines appear in the text as FEIS printed them,
  but no photographs are included.
- **Search vectors:** produced with Google's EmbeddingGemma-300M. Under the
  Gemma Terms of Use, "Google claims no rights in Outputs you generate using
  Gemma", and outputs are not model derivatives.

## The core download (release `core-2026-11`)

Its own `licenses/` folder (assets `core--licenses__*`) holds the full texts;
`NOTICE.txt` there lists every source. In short:

- **`Qwen3-1.7B-Q4_K_M.gguf`:** Qwen3-1.7B by the Qwen team, Apache License
  2.0 (`APACHE-2.0.txt`). Unmodified.
- **`embeddinggemma-300M-Q8_0.gguf`:** Google EmbeddingGemma 300M, unmodified.
  Gemma is provided under and subject to the Gemma Terms of Use found at
  ai.google.dev/gemma/terms (copy: `GEMMA-TERMS-OF-USE.txt`). Its use is
  subject to the Gemma Prohibited Use Policy (`GEMMA-PROHIBITED-USE-POLICY.txt`),
  which binds everyone who uses Fred.
- **Guides (`packs/core-*`):** public-domain US Government sources (US Army
  ATP 4-02.11, ATP 3-50.21, FM 21-76; CDC, NIH, EPA, FDA, National Park
  Service, National Weather Service, Forest Service, BLM, US Public Health
  Service); WHO/ICRC *Basic Emergency Care* (2018), **CC BY-NC-SA 3.0 IGO,
  non-commercial use only**, in `core-firstaid` and the field cards that quote
  it; Wikivoyage articles, CC BY-SA 4.0, in `core-tips-wikivoyage`.
