# Pilot Logbook v2.2 — import z prywatnego Google Sheets

## Co dodano
- Import CSV z arkusza `Pilot Logbook - Verified Flights Inbox` / karta `Flights`.
- Dodawane są tylko nowe wpisy; import pomija istniejące `ImportKey` i duplikaty data + numer lotu + trasa.
- Istniejące wpisy nie są nadpisywane. Zrób kopię JSON przed importem.

## Ograniczenie
To jest bezpieczny import ręczny CSV, nie automatyczna synchronizacja OAuth. Aplikacja nie otrzymuje dostępu do prywatnego arkusza i nie ma żadnego tokena w publicznym repozytorium. Sprawdź czasy, typ samolotu, IFR, lądowania i role przed użyciem jako oficjalnego logbooka.

## Wdrożenie na GitHub Pages
Zastąp w repozytorium pliki `index.html` i `sw.js` plikami z tego pakietu. Pozostałe pliki nie są zmienione. Po wdrożeniu otwórz aplikację i wybierz „Odśwież aplikację”. Najpierw wyeksportuj kopię JSON z obecnej aplikacji.
