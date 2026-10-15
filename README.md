Pilot Logbook v2.2.42 — BLOCK repair

Root cause fixed: the Verified Flights import created a flight object without a `block` property. This version stores the computed OffBlock-to-OnBlock duration on newly imported records.

It also migrates existing email-imported records that have a sourceId, no workbook sourceSheet, saved depTime/arrTime, and missing/zero block. The duration is computed from those saved times (including crossing midnight, maximum 20 hours), then persisted to localStorage and IndexedDB.

Deploy index.html and sw.js. Export a JSON backup first. Do not replace workbook-data.json for this repair. After deployment, open/reload the app; old affected records should be repaired on startup without needing to import again. Confirm visible version v2.2.42 and check 13 October sectors.
