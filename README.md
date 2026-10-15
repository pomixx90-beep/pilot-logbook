POMIWO logbook v2.2.48 — poprawka tworzenia karty synchronizacji

Przed aktualizacją wyeksportuj kopię JSON z komputera i iPhone’a.

1. W GitHubie zastąp index.html, sw.js i manifest.json plikami z tej paczki. Nie zmieniaj ani nie usuwaj workbook-data.json.
2. Zapisz zmiany przez Commit changes i poczekaj na publikację GitHub Pages.
3. Otwórz aplikację i ponów synchronizację. Karta LogbookSync, która już istnieje, nie powinna być tworzona ponownie.

Poprawka obsługuje też sytuację, gdy dwa urządzenia próbują utworzyć kartę jednocześnie. Składnia JavaScript została sprawdzona; zapis na rzeczywistym arkuszu wymaga testu po wdrożeniu.
