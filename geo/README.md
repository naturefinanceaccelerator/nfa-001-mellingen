# Project boundary plus reference areas

Pending. Save the surveyed boundary here as `boundary.geojson` (WGS84, EPSG:4326),
exported from parcel data in CH1903+/LV95 (EPSG:2056).
Then set `location.boundary` to `geo/boundary.geojson` in `nfa-project.json`.

Reference areas: save the outlines as `reference-areas.geojson` (WGS84, optional `name` per feature),
once their publication is cleared. Then set `location.referenceAreas` to `geo/reference-areas.geojson`
plus `referenceAreasStatus` to `surveyed`.
