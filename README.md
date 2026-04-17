# Irish Post-Primary Schools Map

An interactive map of Irish post-primary schools, built from the Department of Education's ArcGIS REST service. Pan and zoom around Ireland, filter by DEIS status, and search by school name. Click any marker to see school details.

## Usage

Open `postprimary_schools_map.html` directly in a browser (Chrome, Firefox, Safari). No build step or server needed — it fetches live data from the Department of Education on load.

> **Note:** The map will not load inside a sandboxed iframe (e.g. some preview panels). Open the file locally in a full browser window.

## Features

- **DEIS filter** — toggle between All / DEIS (red) / Non-DEIS (blue) schools
- **Name search** — real-time substring search across all school names
- **School popup** — click any marker to see roll number, contact info, school type, ethos, gender, Irish classification, attendance type, fee-paying status, principal, and student numbers (girls/boys)

## Data source

Live GeoJSON from the Department of Education ArcGIS FeatureServer:

```
https://services6.arcgis.com/MmUrOQU5v1he9gfS/arcgis/rest/services/Post_Primary_Schools_Ireland/FeatureServer/6
```

All ~750 post-primary schools are fetched on page load. No data is bundled in the file.

## Libraries

- [Leaflet 1.9.4](https://leafletjs.com/) — interactive map
- [OpenStreetMap](https://www.openstreetmap.org/) — tile layer

## Possible extensions

- Add primary schools layer (endpoint in CLAUDE.md) with a toggle
- Filter by county or local authority
- Cluster markers at low zoom levels (Leaflet.markercluster)
- Choropleth layer showing DEIS share by LEA
