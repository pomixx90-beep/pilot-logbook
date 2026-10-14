PILOT LOGBOOK — STATYSTYKI ROCZNE

Zawartość: index.html i sw.js. Wersja nie zawiera workbook-data.json, aby nie nadpisać danych ani źródłowej bazy importu.

WDROŻENIE NA GITHUB PAGES (iPhone):
1. Najpierw zachowaj kopię zapasową lotów w aplikacji: Import / eksport → eksport JSON.
2. Rozpakuj ZIP na urządzeniu.
3. W repozytorium pomixx90-beep/pilot-logbook zastąp plik index.html plikiem z paczki i zatwierdź zmianę.
4. Zastąp plik sw.js plikiem z paczki i zatwierdź zmianę.
5. Poczekaj na publikację GitHub Pages, zamknij kartę aplikacji i otwórz ją ponownie w zwykłej (nieprywatnej) karcie Safari.

WAŻNE: nie zastępuj workbook-data.json i nie importuj ponownie Excela. Aplikacja zapisuje bieżące loty lokalnie w przeglądarce. Aktualizacja kodu nie powinna kasować lokalnych wpisów. Tryb prywatny Safari ma osobny magazyn danych.

Zmiany: statystyki roczne wyliczane z zapisanych lotów; wybór roku na podstawie dat lotów; zestawienie miesięczne, typów samolotów, rejestracji, destynacji i czasu według funkcji; nowy cache service workera.
