# Jamaica Parish Map

An interactive map of Jamaica that runs entirely in the browser. It shows all 14 parishes, roads, towns, landmarks, satellite imagery, elevation and the 2022 census, with tools for measuring, elevation profiles, nearest services and flood-height exposure.

**Live site:** `https://<your-username>.github.io/<repository-name>/` (after you turn on GitHub Pages, below)

## Features

- **Backgrounds:** street-map style, Sentinel-2 satellite (Jul–Sep 2026), elevation tints, historic counties
- **Layers:** main and local roads with route numbers, rivers, towns and villages, landmarks, caves, hill shading, 100 m contours, building density, latitude/longitude grid
- **Search** for about 3,900 towns, villages, landmarks and census communities
- **Parish cards:** capital, county, area, 2022 population, density, growth since 2011, dwellings, and features mapped in OpenStreetMap
- **Tools:** distance, area, elevation profile, and nearest hospital, clinic, pharmacy, police, fire station, school and fuel, with distance rings
- **Flood height:** shades sea-connected land below a chosen level (0–30 m) and estimates the buildings and people affected
- **Population:** parishes shaded by people, density or growth, plus sized circles for 545 census communities
- **2016 vs 2026:** a drag-to-compare satellite view
- **3D terrain:** rotate and zoom the island with adjustable height exaggeration
- **Shareable links:** `#st-ann`, `#ocho-rios`, `#blue-mountain-peak` and similar open straight to a parish or place

## Publish it with GitHub Pages

1. Sign in at [github.com](https://github.com) and create a new repository (for example `jamaica-map`). On a free account, it must be **Public** for Pages to work.
2. On the repository page, choose **Add file → Upload files**, drag in every file from this folder, and click **Commit changes**.
3. Open **Settings → Pages**. Under **Build and deployment**, set **Source** to *Deploy from a branch*, choose the **main** branch and the **/ (root)** folder, and click **Save**.
4. After a minute or two, the site appears at `https://<your-username>.github.io/<repository-name>/`.

The `.nojekyll` file is optional. It tells GitHub Pages to serve the files as they are. macOS hides files whose names start with a dot, so if it doesn't upload, the site still works.

## Files

| File | What it is |
|---|---|
| `index.html` | The map page, with roads, places, boundaries, census figures and contours built in |
| `sat.jpg` | Satellite image, Jul–Sep 2026 |
| `sat2016.jpg` | Satellite image, Jul–Sep 2016 |
| `gap2016.png` | Areas with no clear 2016 view (cloud cover) |
| `elev.png` | Elevation grid (encoded heights, about 120 m per pixel) |
| `bld.png` | Building count per grid cell |
| `par.png` | Parish grid used for population estimates |

The page loads its map and 3D libraries (Leaflet 1.9.4 and three.js r128) from cdnjs, and its fonts from Google Fonts. No server, database or account is needed.

## Not included

- **Shared notes:** the notes feature relies on storage that exists only in the Claude-hosted version, so it is switched off here. It could be reconnected to a database service such as Supabase or Firebase.
- **Source data and processing scripts:** the raw OpenStreetMap extract, satellite and elevation downloads, and the scripts that built these files are kept separately.

## Data sources and credits

Keep these credits wherever the map is shown or shared.

- **Roads, places, buildings and boundaries:** © OpenStreetMap contributors, available under the [Open Database License (ODbL)](https://www.openstreetmap.org/copyright). Extract dated 29 October 2026.
- **Satellite imagery:** contains modified Copernicus Sentinel data 2016 and 2026 (Sentinel-2 quarterly cloudless mosaics).
- **Elevation:** Copernicus DEM GLO-90, © DLR e.V. 2010–2014 and © Airbus Defence and Space GmbH 2014–2018, provided under COPERNICUS by the European Union and ESA. All rights reserved.
- **Population:** Statistical Institute of Jamaica (STATIN), Population and Housing Census 2022.

## Limitations

- Distances are straight-line, not driving routes.
- Elevation is from a 90 m model. Flood shading is a simple height-based estimate, not a flood forecast.
- Facility and building counts reflect what volunteers have mapped in OpenStreetMap and may be incomplete, especially in rural areas.
- 227 census communities (about 26% of people) could not be placed on the map, but they still count in parish totals and flood estimates.
- This map is for information only. It is not a land survey, title search, valuation or engineering assessment.

## License

No license is granted for the map's code and design unless a `LICENSE` file is added to this repository. The data credited above remains under its own licenses.
