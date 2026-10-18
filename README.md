POMIWO Logbook v2.2.69 — naprawa źródłowych statystyk Excela

Co naprawiono:
- Historia źródłowa jest odtwarzana z wierszy arkuszy rocznych, a nie z niekompletnej tablicy `flights`.
- Każdy wiersz Excela identyfikuje para `sourceSheet` + `sourceRow`; nie scala się odrębnych sektorów po podobieństwie.
- Naprawiono daty z błędnym 3-cyfrowym rokiem na podstawie nazwy arkusza.
- Formuły `SUMIF` obsługują kryteria `B737-*`, `B737-8*` i `B737-800`, co przywraca Multi-pilot/IFR.
- `SE`, `ME`, Multi-pilot oraz starty/lądowania dzień/noc odczytywane są z właściwych kolumn arkusza.
- Dla rekordów e-mailowych B737 bez wiersza Excela `ME` i `Multi-pilot` liczone są z block time.
- Kolumny startów/lądowań oraz SBH z Excela nie są nadpisywane przez przybliżenia z maili; e-mail nadal nadpisuje dane sektora, takie jak numer lotu, rejestracja, czasy i dostępne funkcje.
- Loty z 13.10 nie są blokowane: jeśli są w Excelu, pochodzą z jego wierszy; jeśli są wyłącznie z maila, pozostają jako rekordy mailowe.

Wdrożenie:
1. Rozpakuj ZIP do nowego folderu.
2. Podmień `index.html` i `sw.js` na hostingu. Zostaw `workbook-data.json` z tego pakietu (zawiera surowe wiersze arkuszy).
3. Otwórz aplikację ponownie. Na hostingu odśwież stronę; lokalnie otwórz nowy `index.html`.
4. Wersja importu 34 odbudowuje źródłowe loty; dotychczasowe rekordy e-mailowe są dopasowywane po dacie/trasa/rejestracji.

Uwaga: nie usuwaj ręcznie lokalnych danych bez kopii zapasowej. Pełne porównanie z sumami Excela należy wykonać po odbudowie i po synchronizacji e-maili, ponieważ nie mam bezpośredniego dostępu do Twojej bieżącej bazy przeglądarki/Google Sheets.
