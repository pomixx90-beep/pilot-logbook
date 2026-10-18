POMIWO Logbook v2.2.71 — naprawa pominiętego sektora i SBH

Ustalenie: w źródle 2025, wiersz 169, jest lot 2025-06-09 LPDPL → EPPO, 15:48–17:28, BLOCK 1:40, B737-800, SP-RSS. Import odrzucał go wyłącznie dlatego, że LPDPL ma 5 znaków, a walidacja akceptowała tylko 4. Ten rekord odpowiada różnicy 1:40 w nalocie/SIC/IFR/ME/Multi-pilot oraz jednemu brakującemu lądowaniu/startowi.

Zmiany:
- Nie odrzucaj rekordu źródłowego tylko z powodu długości kodu lotniska; lot z czasem i datą zachowuje swój czas i statystyki. Kod źródłowy LPDPL pozostaje bez zmian — nie zgaduję, jaki kod powinien być wpisany w Excelu.
- Dla wpisów powiązanych z wierszem Excela kategorie PIC/SIC, Dual, Instructor, SE/ME, Multi-pilot, IFR, NIGHT i starty/lądowania są ponownie odczytywane z właściwego wiersza źródłowego. Numery lotów, rejestracje i czasy z e-maili nadal uzupełniają dane lotu.
- SBH jest prezentowane tylko raz w nagłówku danego dnia. Jeśli wiele rekordów ma SBH, preferowana jest wartość z wiersza źródłowego Excela zamiast sumowania duplikatów.
- Zwiększono wersję importu i cache service workera.

Wdrożenie lokalne: rozpakuj ZIP do nowego folderu i otwórz index.html. Na hostingu podmień index.html i sw.js; zachowaj workbook-data.json (dołączony plik JSON ma osadzony w index.html odpowiednik). Nie kasuj danych w przeglądarce bez kopii.
