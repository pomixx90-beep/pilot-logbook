Pilot Logbook v2.2.40 — test import BLOCK from email

IMPORTANT: this is a temporary test package. It intentionally removes 13.10.2026 from workbook-data.json so those sectors can be tested from Verified Flights email import. Keep a backup of your current workbook-data.json and restore the full source after the test.

Changes:
- removed 5 workbook flights dated 2026-10-13 from workbook-data.json (and corresponding rows in the 2026 sheet payload);
- bumped app/import/cache version;
- Verified Flights import now updates an existing dated sector by date + route + normalized registration even if the Excel record has no flight number;
- BLOCK is calculated from OnBlock - OffBlock, and existing matching entries are updated rather than silently left at 0:00.

Deploy index.html, sw.js, and workbook-data.json together. Export a JSON backup first.
