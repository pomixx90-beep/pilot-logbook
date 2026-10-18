# POMIWO Logbook v2.2.59 — prevent bulk re-download during sync

- Waits for local recovery and workbook initialization before starting Google synchronization.
- If the previous import marker exists but local flights are empty, reloads workbook data instead of assuming local data is present.
- Stops synchronization with a clear error if the local logbook remains empty, avoiding a bulk pull of the entire cloud history.
- Defines remote source IDs before they are used in duplicate checks.
- Reports merged existing flights separately from genuinely new cloud downloads.
- Updates visible version labels and Service Worker cache version.

Deployment: back up local JSON first. Replace index.html and sw.js in GitHub Pages. Keep workbook-data.json next to index.html; do not replace it with an older copy. Keep manifest.json. Refresh the app after deployment.
