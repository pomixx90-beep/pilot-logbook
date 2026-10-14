# Pilot Logbook — Reports update

This package adds a Reports section inspired by the reference app:
- Time summary and time by role/condition
- Airfields (departures, arrivals, operations)
- Routes with links to Google Maps
- Aircraft registrations and aircraft types
- People / captains with sectors, block time, and share of total time
- Approaches placeholder, because the current source data does not contain approach type/count fields

It also increments the workbook import version to refresh workbook-derived captain and time fields, and increments the service-worker cache version.

## Deploy
Replace `index.html` and `sw.js` in the root of the GitHub Pages repository. Keep `workbook-data.json`, `manifest.json`, and the icons in place. Export a JSON backup before deploying. The app remains local-only; this package does not add cloud sync.
