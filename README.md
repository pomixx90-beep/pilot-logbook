# Pilot Logbook v2.2.21

Reguła importu Verified Flights:
- `TakeOffPilot` zgodny z ustawionym Crew Code: zaznacza PIC; jeśli dowódca jest inny niż `SELF`, zapisuje także PICUS równy block time.
- `TakeOffPilot` inny niż Crew Code: zaznacza Co-pilot/SIC, bez PICUS.
- `LandingPilot` nie wpływa na klasyfikację.

Przed aktualizacją wyeksportuj kopię JSON. Wgraj `index.html` i `sw.js` do katalogu głównego repozytorium GitHub, zastępując poprzednie pliki.
