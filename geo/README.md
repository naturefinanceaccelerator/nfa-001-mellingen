# Project boundary plus reference areas

Pending. Save the surveyed boundary here as `boundary.geojson` (WGS84, EPSG:4326),
exported from parcel data in CH1903+/LV95 (EPSG:2056).
Then set `location.boundary` to `geo/boundary.geojson` in `nfa-project.json`.

Reference areas: `reference-areas.geojson` (WGS84, optional `name` per feature). One point so far.
Replace a point by its outline once the outline may be published.

Project sites (Äbereich, Letzi) are listed as points in `location.sites` in `nfa-project.json`.
