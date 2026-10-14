# Pilot Logbook v2.2.6 — poprawka importu Verified Flights

Ta wersja:
- zmienia widoczny numer wersji na v2.2.6;
- rozpoznaje nagłówki Excela niezależnie od spacji, podkreśleń i wielkości liter;
- pobiera godziny z kolumn Off Block / On Block i konwertuje je do HH:MM;
- zachowuje funkcję FO jako Co-pilot (SIC); pilotowanie startu lub lądowania nie oznacza funkcji PIC;
- zapisuje informacje Pilot Flying, Takeoff pilot i Landing pilot w uwagach.

Przed wdrożeniem wyeksportuj kopię JSON. Wgraj `index.html` i `sw.js` do głównego katalogu repozytorium, zastępując istniejące pliki, i wykonaj Commit changes.
