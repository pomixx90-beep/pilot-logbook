POMIWO logbook v2.2.51 — poprawka testowa dla 11.10.2026

Co poprawiono:
- usunięto loty z 2026-10-11 z dołączonego workbook-data.json;
- podbito wersję importu, żeby aplikacja odświeżyła rekordy z pliku źródłowego;
- przy starcie usuwa z lokalnej bazy i kopii IndexedDB wyłącznie loty z 2026-10-11;
- import Verified Flights pomija tę datę;
- synchronizacja usuwa z karty LogbookSync rekordy chmurowe z tą datą, żeby nie wracały na urządzenie;
- poprawiono wersję cache service workera.

Wdrożenie: zrób kopię JSON aktualnych lotów. W repozytorium GitHub Pages zastąp index.html, sw.js, manifest.json oraz workbook-data.json plikami z paczki. Commit/push, poczekaj na publikację, a potem w aplikacji kliknij „Odśwież aplikację” i „Połącz Google Sheets / synchronizuj”.

Uwaga: jest to celowe czyszczenie testowe dla daty 11.10.2026. Nie używaj tej wersji, jeśli chcesz zachować jakiekolwiek prawdziwe loty z tej daty.
