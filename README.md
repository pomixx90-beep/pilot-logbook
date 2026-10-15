POMIWO logbook v2.2.49 — poprawka odczytu karty Flights

Przed aktualizacją wyeksportuj kopię JSON z komputera i iPhone’a.

W GitHubie zastąp tylko index.html, sw.js i manifest.json plikami z tej paczki. Nie zmieniaj ani nie usuwaj workbook-data.json, nie usuwaj вкладки Flights и LogbookSync. Commit changes i poczekaj na publikację GitHub Pages.

Poprawka najpierw odczytuje jawny zakres 'Flights'!A1:AZ1000, a następnie próbuje poprzedniego zakresu. Jeśli API ponownie zwróci pusty wynik, aplikacja pokaże nazwę pliku i listę kart, co ułatwi ustalenie przyczyny. Składnię należy sprawdzić przed publikacją; rzeczywisty dostęp do Google Sheets nie został tu przetestowany.
