# POMIWO Logbook v2.2.78 — poprawka trwałości SBH

## Poprawki
- Widoczna wersja aplikacji w nagłówku, podsumowaniu, stopce i tytule strony: `v2.2.78`.
- Zwiększono cache Service Workera do `pomiwo-logbook-v2.2.78` i wersję odbudowy historii do `39`.
- Naprawiono utratę `sectorSBH` podczas ponownego budowania historii z danych Excela po odświeżeniu.
- `sectorSBH` jest teraz kopiowane z zachowanych wpisów e-mail do odpowiadającego im wiersza Excela.
- Dla poprzednich danych, w których `sectorSBH` już zniknęło lokalnie, wartość jest odzyskiwana z zachowanych `scheduledSTD` i `scheduledSTA` (STA − STD).
- Pusta lub zerowa wartość ze starego wpisu nie kasuje dodatniego SBH sektora.
- Poprzednia normalizacja kodu `LPDPL` → `LDPL` i synchronizacja do `LogbookSync` pozostają w tej wersji.

## Wdrożenie
Wgraj wszystkie pliki z tego archiwum do katalogu głównego aplikacji, nadpisując `index.html`, `workbook-data.json`, `sw.js` i `manifest.json`. Otwórz aplikację online i sprawdź widoczny numer `v2.2.78`. Uruchom synchronizację raz, odśwież i sprawdź SBH bez ponownej synchronizacji.
