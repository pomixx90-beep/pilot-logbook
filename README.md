Pilot Logbook v2.2.29 — import and dashboard totals repair

Files to replace in the GitHub Pages repository:
- index.html
- sw.js

Before updating, export a JSON backup from the app. After replacing both files, commit the changes and wait for GitHub Pages to publish. Confirm the visible app version is v2.2.29.

Changes:
- Prevents the synthetic-training DATE header later in the Excel header from overriding the actual flight date column. This was the primary reason historical rows could not be matched and their departure/arrival times and takeoff/landing counts remained blank.
- Reads Excel clock values from numeric fractions and ISO-like serialized date values.
- Maps SE and ME marks ('x') to the row's block time, reads multi-pilot time separately, and fixes the ME classification regex.
- Removes the duplicate 'Nalot całkowity' card from the added summary because the main Dashboard already has that tile.
- Refreshes workbook import version and service-worker cache version.

Note: the source workbook-data.json remains in the repository and is not included in this ZIP. The importer reads it from GitHub Pages.
