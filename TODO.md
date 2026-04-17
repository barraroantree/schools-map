# Schools Map — To Do

## Primary schools layer
- [ ] Add primary schools from `MainstreamPrimarySchoolsIreland/FeatureServer/0`
- [ ] Fetch actual field names from that endpoint (likely differ from post-primary)
- [ ] Add toggle in header to show/hide primary vs post-primary layer
- [ ] Use distinct marker style (e.g. square vs circle, or different colour palette)
- [ ] Check whether DEIS and gender fields are present and consistent

## Filtering overhaul
- [ ] Replace DEIS/Non-DEIS buttons with a filter panel or dropdown set
- [ ] Filter by gender: All / Boys / Girls / Mixed
- [ ] Filter by school type (using `Post_Primary_School_Type` field values from data)
- [ ] Filter by fee-paying status
- [ ] Allow combining filters (e.g. DEIS + Girls)
- [ ] Keep DEIS as an option alongside the new filters rather than removing it

## Map improvements
- [ ] Add marker clustering at low zoom levels (Leaflet.markercluster plugin)
- [ ] Filter by county using a dropdown — field `County` is in the data, just skipped from popup
- [ ] Show a count badge on the filter buttons (e.g. "Girls · 120")
- [ ] Add a "locate me" button to centre the map on the user's location

## Popup / data
- [ ] Join feeder school progression rate data (`data-E5DbG.csv`) via Roll Number to show progression rates in popup
- [ ] Check whether a school website field exists in either endpoint and add it back if so
- [ ] Show academic year of the data in the popup or page footer

## Deployment / housekeeping
- [ ] Rename `postprimary_schools_map.html` → `index.html` for cleaner GitHub Pages URL
- [ ] Add a note to README with the live GitHub Pages URL once confirmed working
