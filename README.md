# POMIWO Logbook v2.2.77 — poprawka lotniska i trwałej synchronizacji

## Poprawki
- Widoczna wersja w nagłówku, podsumowaniu i stopce to teraz `v2.2.77`.
- Błędny kod z maila `LPDPL` jest normalizowany do `LDPL` przy imporcie, normalizacji lokalnych rekordów, odczycie rekordów chmurowych i budowaniu danych z Excela.
- Rekord z 09.06.2025 (`LDPL → EPPO`, SP-RSS) dopasowuje się do wiersza Excela zamiast tworzyć osobny lot z literówką. Źródłowy BLOCK pozostaje 1:40.
- Dane z aktualnie odczytanej karty `Flights` mają pierwszeństwo nad starszym ładunkiem `LogbookSync` dla tego samego ImportKey.
- Po scaleniu aplikacja zapisuje zaktualizowany `PayloadJSON` do istniejących wierszy `LogbookSync`, aby kolejna synchronizacja/odświeżenie nie przywracały starej trasy ani starych pól.
- Zwiększono wersję importu do `38` i cache Service Workera do `pomiwo-logbook-v2.2.77`. Przycisk odświeżania czeka na aktywację aktualizacji Service Workera.

## Wdrożenie
Wgraj wszystkie pliki z tego folderu do katalogu głównego aplikacji, nadpisując: `index.html`, `workbook-data.json`, `sw.js`, `manifest.json`. Po wdrożeniu otwórz aplikację online, sprawdź plakietkę `v2.2.77`, wykonaj synchronizację i ponownie odśwież stronę. W przypadku Google Sheets aktualizacja zapisuje też poprawioną treść do karty `LogbookSync`.
