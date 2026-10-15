# POMIWO logbook v2.2.44

Zmiany:
- nazwa aplikacji zmieniona na POMIWO logbook; manifest PWA z nazwą POMIWO,
- przycisk „＋ Dodaj lot” przeniesiony do prawego górnego rogu nagłówka,
- gest przeciągnięcia w dół na iPhonie od samej góry strony uruchamia odświeżenie aplikacji,
- zwiększona wersja aplikacji i cache service workera.

Wdrożenie: przed zmianą wyeksportuj JSON. W GitHub podmień `index.html`, `sw.js` i `manifest.json`. Nie zmieniaj `workbook-data.json`. Zachowuje to poprawki BLOCK/SBH z v2.2.43.

Po wdrożeniu na iPhonie odśwież stronę. Jeśli aplikacja jest dodana do ekranu początkowego, zamknij ją i uruchom ponownie, aby iOS pobrał nową nazwę manifestu.
