# Hampton Roads Seven Cities Map

An interactive web map of the seven independent cities of the Hampton Roads Metropolitan Area, Virginia. Built with Leaflet.js and OpenStreetMap, using embedded Census TIGER/Line boundary data and 2020 Census population statistics.

🗺️ **[View Live Map](https://jessicacevans.github.io/hampton-roads-map/)**

---

## Cities Included

| City | FIPS | Population (2020) | Land Area (sq mi) |
|---|---|---|---|
| Portsmouth ★ | 51740 | 95,535 | 33.0 |
| Norfolk | 51710 | 238,005 | 53.8 |
| Virginia Beach | 51810 | 459,470 | 248.3 |
| Chesapeake | 51550 | 249,422 | 340.8 |
| Hampton | 51650 | 137,148 | 51.5 |
| Newport News | 51700 | 186,247 | 69.4 |
| Suffolk | 51800 | 97,284 | 400.0 |

★ Portsmouth is the home city and primary focus of this map.

---

## Features

- Interactive Leaflet.js map with OpenStreetMap basemap
- **Reset View** button — returns the map to Portsmouth at zoom 12
- Pan and zoom constrained to the Hampton Roads region
- Click any city polygon to view population, land area, and population density
- Clickable legend that zooms to each city
- Earth tone color palette with Portsmouth highlighted in deep rust red
- Fully self-contained — no external API calls, all boundary data embedded

---

## Data Sources

| Data | Source |
|---|---|
| City boundaries | U.S. Census Bureau TIGER/Line geographic identifiers, decoded from us-atlas TopoJSON |
| Population | 2020 Census P.L. 94-171 Redistricting Data Summary File (Table P1) |
| Land area | U.S. Census Bureau TIGER/Line geographic identifiers (sq mi) |
| Basemap | © [OpenStreetMap](https://www.openstreetmap.org/copyright) contributors, ODbL |

---

## Tech Stack

- [Leaflet.js](https://leafletjs.com/) 1.9.4
- OpenStreetMap tiles
- Vanilla HTML / CSS / JavaScript — no build tools required
- Embedded GeoJSON (Census TIGER/Line derived, simplified for visualization)

---

## Deployment

This map is hosted via **GitHub Pages** and embedded in Squarespace via an iframe.

### Run locally

Simply open `index.html` in any web browser — no server required.

### GitHub Pages

1. Push `index.html` to the root of a public GitHub repository
2. Go to **Settings → Pages → Deploy from branch (main / root)**
3. Your map will be live at `https://jessicacevans.github.io/hampton-roads-map/`

### Embed in Squarespace

```html
<iframe
  src="(https://jessicacevans.github.io/hampton-roads-map/)"
  width="100%"
  height="750"
  style="border:none;"
  loading="lazy"
  title="Hampton Roads Seven Cities Map">
</iframe>
```

---

## Repository Structure

```
/
├── index.html        # Self-contained map application
└── README.md         # This file
```

---

## Notes on Geometry

Polygon boundaries are simplified representations derived from Census TIGER/Line data, intended for visualization purposes. For spatial analysis, use the full-resolution Census TIGER/Line FIPS-keyed shapefiles joined to ACS data by GEOID (text field — preserve leading zeros).

---

## Contributors

Google Earth · ESRI · NAVFAC

---

## License

MIT License

Copyright (c) 2026 Jessica Evans

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.

This project is released for public use. Boundary data is U.S. government public domain. Basemap tiles © OpenStreetMap contributors under [ODbL](https://opendatacommons.org/licenses/odbl/).
