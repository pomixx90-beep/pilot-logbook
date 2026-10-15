# Pilot Logbook v2.2.22 — Verified Flights time fix

Poprawia odczyt godzin z plików Excel, które zwracają czas w formacie 12-godzinnym, np. `04:14 AM` / `05:38 AM`. Importer normalizuje je do UTC `04:14` / `05:38`, a następnie wylicza przybliżony czas nocny oraz checkboxy dzień/noc startu i lądowania.

Wgraj `index.html` i `sw.js` do głównego katalogu repozytorium GitHub Pages. Przed aktualizacją wyeksportuj kopię JSON. Duplikaty nie są ponownie importowane; istniejące wpisy wymagają osobnej edycji, jeśli godziny są puste.
