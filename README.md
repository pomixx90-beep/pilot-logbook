# POMIWO Logbook v2.2.60

Poprawka deduplikacji lotów Excel/e-mail i lokalnego scalania podczas startu oraz synchronizacji.

## Wdrożenie
1. Zrób kopię danych logbooka.
2. Podmień `index.html` i `sw.js` w GitHub Pages.
3. Pozostaw istniejące `workbook-data.json` i `manifest.json`.
4. Opublikuj zmiany i odśwież aplikację.

Nie czyść pamięci przeglądarki. Deduplikacja scala rekordy tego samego dnia i trasy, z tą samą rejestracją (jeśli jest dostępna), zgodnym numerem lotu (jeśli oba wpisy go mają), zbliżonym czasem BLOCK oraz kompatybilnymi godzinami. Zachowuje rekord Excela jako podstawowy i uzupełnia go danymi e-maila.
