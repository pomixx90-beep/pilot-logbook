POMIWO logbook v2.2.56 — zachowanie SBH i korekta zduplikowanych statystyk

Poprawki: (1) wartość SBH=0 z Excela nie nadpisuje wcześniejszego dodatniego SBH; (2) dokładnie powielone wiersze arkusza nie są liczone drugi raz, a przy scalaniu zachowywane są dodatnie SBH i inne czasy; (3) zachowane jest wyświetlanie SBH dla lotów z Excela.

Wdrożenie: zrób kopię danych, podmień index.html i sw.js w GitHub Pages, commituj, poczekaj na publikację i kliknij „Odśwież aplikację”.

Ważne: zrób kopię JSON przed wdrożeniem. Wersja importu 28 odtworzy rekordy z workbook-data.json, zachowa dodatnie SBH z poprzednich rekordów o tych samych ID i pominie tylko dokładne duplikaty (data, trasa, rejestracja, godziny i block). Synchronizacji Google nie testowano.
