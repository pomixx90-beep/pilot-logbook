# POMIWO Logbook v2.2.76 — poprawka synchronizacji

Zmiany:
- Poprawiono błędny kod lotniska `LPDPL` na `LDPL` w źródłowych danych Excela i wbudowanym fallbacku.
- Podbito wersję importu danych do 37, aby aplikacja przebudowała dane z poprawionego źródła i zachowała nakładki z maili.
- Podbito nazwę cache Service Workera.
- Usunięto z listy pre-cache ikonki, których nie było w paczce; poprzedni `cache.addAll()` mógł przez to odrzucać instalację Service Workera.

Wdrożenie: wgraj wszystkie pliki z folderu paczki do tego samego katalogu na hostingu, nadpisując istniejące. Nie wgrywaj tylko `index.html` — wymagane są również `workbook-data.json` i `sw.js`. Następnie zamknij aplikację i otwórz ją ponownie online. Po synchronizacji sprawdź, czy lot z 09.06.2025 ma trasę `LDPL → EPPO` i BLOCK `1:40`, a po odświeżeniu dane pozostają.
