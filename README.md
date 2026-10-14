# Pilot Logbook PWA — updated flight-entry form

This package updates the flight-entry form while preserving the existing imported workbook data.

- Block time is calculated from off-block and on-block times entered in UTC (including overnight flights).
- Boeing aircraft types automatically set IFR time equal to block time as requested; check this against the actual flight conditions before relying on the entry.
- Pilot functions are selectable with checkboxes: PIC, Co-pilot, Dual, Instructor. Selected function time is set to block time and can be adjusted if only part of the flight applies.
- Night time remains editable and is not guessed automatically. EASA defines night as the period between the end of evening civil twilight and the beginning of morning civil twilight, or another period prescribed by the competent authority; there is no universal EASA rule that simply adds/subtracts 30 minutes from block time.
- Existing flight data and workbook-data.json are retained. No import version bump is performed, to avoid overwriting local entries.

Upload the files to the root of the GitHub Pages repository, replacing index.html and sw.js (other files can remain unchanged).
