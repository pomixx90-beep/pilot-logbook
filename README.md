Pilot Logbook v2.2.27 — JSON repair package

Contains:
- index.html: increments app version and workbook import version to force re-import.
- sw.js: cache version update.
- workbook-data.json: repaired workbook-derived flight fields, including departure/arrival times, SE/ME, multi-pilot time, takeoffs and landings.

Before replacing files, export a JSON backup from the app.
Replace index.html, sw.js, and workbook-data.json in the GitHub repository. Commit all three together.
This package preserves the 973 existing workbook flight IDs by source row identity but changes their IDs to force stale records to be refreshed. Manually created entries are intended to be retained by the app's source/manual filtering.
