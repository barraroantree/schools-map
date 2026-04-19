# Irish Schools & Childcare Map

An interactive map of Irish primary schools, post-primary schools, and childcare facilities. Pan and zoom around Ireland, filter by various criteria, and search by name. Click any marker to see details.

## Live maps

View the deployed maps on GitHub Pages:

- [Primary schools](https://barraroantree.github.io/schools-map/primary_schools_map.html)
- [Post-primary schools](https://barraroantree.github.io/schools-map/postprimary_schools_map.html)
- [Childcare facilities](https://barraroantree.github.io/schools-map/childcare_map.html)

## Usage

Open any HTML file directly in a browser (Chrome, Firefox, Safari). No build step or server needed — each file fetches live data on load.

> **Note:** The maps will not load inside a sandboxed iframe (e.g. some preview panels). Open the files locally in a full browser window.

## Files

| File | Description |
|------|-------------|
| `primary_schools_map.html` | ~3,300 mainstream primary schools |
| `postprimary_schools_map.html` | ~750 post-primary schools |
| `childcare_map.html` | Childcare facilities from Pobal |

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

### Childcare
- **Marker colour** — teal for community/voluntary, amber for private, grey for other
- **Programme filters** — toggle ECCE, CCSP, and NCS to show only participating facilities
- **Organisation type dropdown** — populated dynamically from the data
- **Name search** — real-time substring search
- **Facility popup** — eircode, phone, email, organisation type, and ECCE/CCSP/NCS participation

## Data sources

**Schools** — live GeoJSON from the Department of Education ArcGIS FeatureServer:

```
Primary:      MainstreamPrimarySchoolsIreland/FeatureServer/0
Post-primary: Post_Primary_Schools_Ireland/FeatureServer/6
```

(Both under `https://services6.arcgis.com/MmUrOQU5v1he9gfS/arcgis/rest/services/`)

**Childcare** — live GeoJSON from the Pobal ArcGIS FeatureServer:

```
Childcare_Facilities_NEW/FeatureServer/2
```

(Under `https://services8.arcgis.com/AF8wcIoCeDo33LsM/arcgis/rest/services/`)

## Libraries

- [Leaflet 1.9.4](https://leafletjs.com/) — interactive map
- [OpenStreetMap](https://www.openstreetmap.org/) — tile layer
