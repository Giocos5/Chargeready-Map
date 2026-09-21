# ChargeReady Market Map

An interactive field map for reviewing ChargeReady opportunities across Ameren Illinois territory, with a focused view of eligible multifamily properties in Champaign and Urbana.

**Live map:** <https://giocos5.github.io/Chargeready-Map/>

## What the map shows

The map opens over Champaign–Urbana and displays researched apartment and manufactured-home communities by unit or site count. Every map group can be expanded, and every sublayer has its own checkbox.

The property-size classes are:

- **250+ units/sites** — red
- **150–249 units/sites** — orange
- **75–149 units/sites** — yellow
- **Under 75 units/sites** — green
- **Count needs verification** — gray

Marker size also increases with property size. Clicking or hovering over a property displays its name, verified address, property type, unit/site count, count basis, confidence level, phone number, and website when available.

## Layer groups

- Properties by Unit Count — Champaign–Urbana
- Multifamily Complexes — Property Types
- Single Family Housing Density
- Straight EV Counts
- Composite Priority Map
- EJC, CEJA, R3, and Income Qualifying Areas
- EV Score — Demand + Trend
- Supporting Layers, including Non-EIEC and Ameren territory
- Basemaps

The Non-EIEC layer uses a 40% transparent fill so the satellite imagery and other layers remain visible.

## Unit-count research

The focused Champaign–Urbana dataset contains 53 valid communities:

- 40 apartment complexes totaling 7,679 units
- 13 manufactured-home communities totaling 1,740 sites or estimated homes

Counts were compiled from state and municipal records, property and developer materials, verified listings, and housing studies. Records using the best available estimate are labeled with medium confidence and appear in the gray verification class. Two false-positive source records were excluded.

## Main files

| File | Purpose |
| --- | --- |
| `index.html` | Leaflet map, controls, styling, popups, and layer behavior |
| `unit_count_properties.geojson` | Champaign–Urbana properties with unit counts and confidence fields |
| `mf_prospects.geojson` | Statewide multifamily prospect points |
| `zip_priority.geojson` | ZIP-level priority and EV score classes |
| `ev_counts.geojson` | ZIP-level EV counts |
| `sf_housing.geojson` | Single-family housing density |
| `ejc.geojson`, `ceja.geojson`, `r3.geojson`, `lmi.geojson` | Eligibility and qualifying areas |
| `non_eiec.geojson` | Ameren territory outside the selected eligibility areas |
| `ameren_territory.geojson` | Ameren Illinois territory |
| `il_boundary.geojson` | Illinois boundary |

## Publishing an update

1. Open the repository on GitHub and select the **Code** tab.
2. Confirm the selected branch is **main**.
3. Select **Add file → Upload files**.
4. Upload the updated files at the repository's top level. Keep the existing filenames so the map can find them.
5. Enter a short description of the update.
6. Select **Commit directly to the main branch** and choose **Commit changes**.
7. Wait for GitHub Pages to rebuild, then refresh the live map. A hard refresh may be needed to clear the browser cache.

Do not upload passwords, API keys, access tokens, private contact lists, or unrelated project files. The published repository should contain only the web map and its public data files.

## Technology

The site is a static HTML map built with [Leaflet](https://leafletjs.com/) and published through GitHub Pages. It does not require a database or server-side application.
