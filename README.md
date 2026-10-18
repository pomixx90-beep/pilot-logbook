POMIWO Logbook v2.2.57 — email overrides matching Excel flights

Poprawka: rekordy z Verified Flights (e-mail) aktualizują dopasowany lot z Excela zamiast tworzyć drugi wpis. Pola dostarczone przez e-mail, w tym BLOCK, SBH, rejestracja, trasa, czasy, flight number i role, mają pierwszeństwo; puste pola e-maila nie kasują istniejących danych Excel. Rekord zachowuje ID wiersza Excel, więc statystyki liczą go tylko raz. Ręcznie dodane loty bez sourceId nie są automatycznie traktowane jak import e-mailowy. Zwiększono wersję importu do 29, aby ponownie wykonać scalanie po wdrożeniu.

Wdrożenie: zrób kopię JSON, podmień index.html i sw.js w GitHub Pages, commituj i po publikacji użyj „Odśwież aplikację”. workbook-data.json musi pozostać obok index.html.

Nie usuwaj danych lokalnych przed kopią zapasową. Synchronizacji Google nie testowano na żywym arkuszu.
