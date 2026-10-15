POMIWO logbook v2.2.52 — naprawa importu lotów z 11.10.2026

Co poprawiono:
- usunięto filtr blokujący import daty 2026-10-11 z karty Flights;
- usunięto automatyczne kasowanie lokalnych lotów z tej daty;
- usunięto automatyczne kasowanie wierszy z datą 2026-10-11 z karty LogbookSync;
- podbito wersję cache Service Workera do v2.2.52.

Wdrożenie:
1. Zrób kopię JSON z aktualnymi lotami.
2. W repozytorium GitHub Pages zastąp index.html i sw.js plikami z paczki. manifest.json nie wymaga zmiany.
3. Zapisz commit i poczekaj na publikację.
4. Otwórz aplikację, kliknij „Odśwież aplikację”, następnie „Połącz Google Sheets / synchronizuj”.
5. Sprawdź status synchronizacji: liczba „nowych” lotów z maili powinna wzrosnąć, jeśli loty z 11.10 są w karcie Flights i nie zostały już zaimportowane.

Nie wykonywano rzeczywistej synchronizacji z kontem Google.
