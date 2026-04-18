# Irish Schools Map

An interactive map of Irish primary and post-primary schools, built from the Department of Education's ArcGIS REST service. Pan and zoom around Ireland, filter by gender, ethos, and more, and search by school name. Click any marker to see school details.

## Live map

View the deployed map on GitHub Pages:  
https://barraroantree.github.io/schools-map/postprimary_schools_map.html

## Usage

Open `primary_schools_map.html` or `postprimary_schools_map.html` directly in a browser (Chrome, Firefox, Safari). No build step or server needed — each file fetches live data from the Department of Education on load.

> **Note:** The maps will not load inside a sandboxed iframe (e.g. some preview panels). Open the files locally in a full browser window.

## Files

| File | Description |
|------|-------------|
| `primary_schools_map.html` | ~3,300 mainstream primary schools |
| `postprimary_schools_map.html` | ~750 post-primary schools |

## Features

### Primary
- **Gender filter** — All / Boys / Girls / Mixed (inferred from enrollment counts where no gender field is present)
- **Irish classification filter** — dropdown populated from the `Irish_Classification_Descriptio` field
- **Name search** — real-time substring search
- **School popup** — roll number, ethos, gender, Irish classification, fee-paying status, DEIS, Gaeltacht indicator, student numbers, and link to inspection reports

### Post-primary
- **Gender filter** — All / Boys / Girls / Mixed
- **Fee-paying filter** — All / Fee paying / Free
- **Type & ethos dropdowns** — populated dynamically from the data
- **Name search** — real-time substring search
- **School popup** — roll number, contact info, school type, ethos, gender, Irish classification, attendance type, fee-paying status, principal, student numbers, and link to inspection reports

## Data sources

Live GeoJSON from the Department of Education ArcGIS FeatureServer:

```
Primary:      MainstreamPrimarySchoolsIreland/FeatureServer/0
Post-primary: Post_Primary_Schools_Ireland/FeatureServer/6
```

(Both under `https://services6.arcgis.com/MmUrOQU5v1he9gfS/arcgis/rest/services/`)

## Libraries

- [Leaflet 1.9.4](https://leafletjs.com/) — interactive map
- [OpenStreetMap](https://www.openstreetmap.org/) — tile layer
