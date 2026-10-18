POMIWO logbook v2.2.54 — deduplikacja lotów mail/Excel

Co zmieniono:
- Podniesiono wersję importu Excela, aby wymusić ponowne uzgodnienie już zapisanych danych.
- Rekordy zaimportowane z maila są łączone z odpowiadającymi im lotami z workbook-data.json na podstawie daty, trasy i rejestracji (normalizacja rejestracji usuwa łączniki/spacje).
- Zamiast wyświetlać osobny lot z numerem i drugi „bez numeru”, zachowywany jest jeden rekord z metadanymi maila.
- Dodano końcowe zabezpieczenie przed duplikatem mail/Excel.

Wdrożenie:
1. Zrób kopię danych lotów.
2. Podmień index.html i sw.js w repozytorium GitHub Pages.
3. Zapisz zmiany i poczekaj na publikację.
4. Otwórz aplikację, wybierz „Odśwież aplikację”.

Uwaga: nie wykonywano rzeczywistej synchronizacji z kontem Google.
