POMIWO logbook v2.2.50 — poprawka aktualizacji trasy z Verified Flights

Przy imporcie aplikacja już odczytuje DepartureICAO i ArrivalICAO w pierwszej kolejności. Błąd polegał na tym, że gdy lot już istniał (dopasowanie po ImportKey), aplikacja aktualizowała m.in. block time i numer lotu, ale nie aktualizowała zapisanej trasy. Dlatego stary wpis mógł pozostać jako EPPO → DBV mimo że arkusz ma EPPO → LDDU.

W tej wersji istniejące wpisy dopasowane po ImportKey aktualizują również datę oraz kody lotnisk z arkusza. Wersja i cache service workera zostały podbite do 2.2.50.

Przed aktualizacją wyeksportuj kopię JSON z komputera i iPhone’a. W GitHubie zastąp pliki index.html, sw.js, manifest.json z tej paczki. Nie zmieniaj ani nie usuwaj workbook-data.json, arkusza Flights ani LogbookSync. Zrób commit i poczekaj na publikację GitHub Pages. Po publikacji w aplikacji kliknij „Odśwież aplikację”, następnie „Połącz Google Sheets / synchronizuj”, aby zaktualizować istniejące wpisy.

Zmiana została sprawdzona pod kątem składni JavaScript; synchronizacja z rzeczywistym arkuszem wymaga uruchomienia w aplikacji.
