# Pilot Logbook — raporty i lądowania

Zmiany w tej wersji:
- podsumowanie Dashboardu przeniesione do Raporty → Czas; Dashboard pokazuje ostatnie loty;
- trasy w obie strony łączone w jeden wiersz z osobnymi sektorami i czasami dla każdego kierunku;
- typ samolotu w ręcznym formularzu to lista Boeing 737-700 / 737-800 / 737-8200;
- lądowania dzień/noc wybierane checkboxami i zapisywane osobno; importowane wartości dzienne/nocne są zachowywane, gdy są dostępne;
- cache service workera zwiększony do nowej wersji.

Czas nocny: nie naliczam go automatycznie z samego off-block/on-block, bo nie są to dokładne czasy take-off/landing ani pozycja samolotu w trakcie lotu. Proponowany mechanizm opisano w odpowiedzi; obecnie pole Night pozostaje ręczne.

Przed podmianą plików wykonaj eksport JSON. W GitHub Pages zastąp index.html i sw.js; pozostaw workbook-data.json, manifest.json i ikony.
