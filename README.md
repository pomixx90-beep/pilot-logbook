POMIWO Logbook v2.2.72 — SBH z e-maili per sektor

Zmiany:
- Wpisy importowane z e-maila pokazują SBH sektora przy danym locie.
- Górny nagłówek dnia pokazuje sumę SBH sektorów dla dni bez źródłowego wpisu Excela.
- Jeśli dzień ma dzienną wartość SBH z Excela, pozostaje ona wartością referencyjną nagłówka; nie sumujemy jej ponownie dla każdego sektora.
- Gdy e-mail aktualizuje rekord Excela, jego SBH sektora jest zachowywane oddzielnie w polu sectorSBH, bez nadpisywania dziennego SBH z arkusza.
- Podniesiono wersję cache do 2.2.72.

Wdrożenie: rozpakuj do nowego folderu i otwórz index.html. Dla hostingu podmień index.html i sw.js; zachowaj manifest i aktualny workbook-data.json.
