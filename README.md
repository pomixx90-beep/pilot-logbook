# Pilot Logbook v2.2.31 — source workbook rebuild

## What changed
- Rebuilt `workbook-data.json` directly from the uploaded `Logbook(1).xlsx`.
- Included 977 rows with a positive block time.
- Corrected four malformed dates that previously caused flights to be skipped:
  - 2020 row 49 → 2020-07-13
  - 2022 row 9 → 2022-04-16
  - 2022 row 32 → 2022-06-10
  - 2024 row 500 → 2024-12-21
- Preserved the actual year-specific column positions for SE/ME, multi-pilot, PIC, co-pilot, Dual, IFR, Night, takeoffs and landings.
- The app no longer recalculates verified JSON fields from raw sheet cells.
- Import/cache version: 19 / v2.2.31.

## Verified against the workbook
- Block time: 2183:31
- PIC: 1003:00
- Co-pilot / SIC: 1092:10
- Dual: 87:37
- IFR: 1998:58
- SE: 169:28
- ME: 2014:03
- Multi-pilot: 1983:19
- Takeoffs day/night: 941 / 217
- Landings day/night: 885 / 273
- Total landings: 1158

## Install
1. Export a JSON backup from the current app first.
2. Replace `index.html`, `sw.js`, and `workbook-data.json` in the GitHub repository with the files in this package.
3. Commit the changes and wait for GitHub Pages to publish.
4. Open the app and confirm it shows v2.2.31. If it still shows an old version, use the app's Refresh app button.
5. Check the dashboard against the totals above.

The import refresh replaces workbook-derived records with the corrected source records and keeps manually added records that do not have `sourceSheet`.
