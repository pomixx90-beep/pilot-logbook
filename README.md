# POMIWO Logbook v2.2.79 — poprawka aktualizacji lotów z zaległych maili

## Zmiany
- Widoczny numer wersji `v2.2.79` w nagłówku, podsumowaniu, tytule i stopce.
- Cache Service Workera zmieniony na `pomiwo-logbook-v2.2.79`.
- Wersja importu danych podbita do `40`.
- Dopasowanie maila najpierw po `ImportKey`, potem po dacie + numerze lotu; dopiero następnie po dacie + trasie + zgodnej rejestracji. Różnice czasu BLOCK nie blokują już mocnego dopasowania po numerze lotu.
- Raport synchronizacji pokazuje oddzielnie, ile wpisów zostało dodanych z maili, a ile istniejących wpisów zaktualizowano z maili. Nie myli tego z liczbą rekordów dopasowanych w chmurze.
- Po imporcie przed scałaniem z chmurą wykonywany jest zapis trwały do lokalnego IndexedDB.
- Zachowano normalizację `LPDPL` → `LDPL` oraz naprawy SBH z poprzednich wersji.

## Wdrożenie
Wgraj wszystkie pliki z archiwum do katalogu głównego aplikacji, nadpisując `index.html`, `workbook-data.json`, `sw.js` i `manifest.json`. Otwórz aplikację online, upewnij się, że nagłówek pokazuje `v2.2.79`, a następnie wykonaj synchronizację. W komunikacie sprawdź liczbę „zaktualizowanych istniejących” lotów z maili. Po odświeżeniu sprawdź te same wpisy ponownie.
