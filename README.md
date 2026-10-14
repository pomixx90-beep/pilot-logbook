# Pilot Logbook v1.9

Zmiany:
- Dashboard: wskaźniki nalotu za 7 i 28 dni, rok kalendarzowy oraz 365 dni.
- 28 dni pokazuje próg 100 h; rok kalendarzowy 900 h; 365 dni 1000 h. Wskaźnik 7 dni jest informacyjny i nie przedstawia limitu duty/FDP.
- Ostatnie loty można dotknąć, aby przejść do edycji wpisu.
- Historia wyszukuje również po nazwisku dowódcy / NAME PIC.
- Raporty → Czas: opcja „Całkowite” obok poszczególnych lat.
- Wersja aplikacji v1.9; nowy cache service workera.

Wdrożenie: zrób kopię JSON, a następnie w katalogu głównym repozytorium podmień index.html i sw.js. Nie podmieniaj workbook-data.json na starszą kopię.

Uwaga: wskaźniki nalotu nie są pełnym kalkulatorem FTL. Zwłaszcza duty, FDP i odpoczynek wymagają osobnych danych i zatwierdzonych zasad operatora.
