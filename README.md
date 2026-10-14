# Pilot Logbook PWA — import lotów z Excela

Aplikacja automatycznie importuje loty z arkuszy rocznych i Winter z dołączonego `workbook-data.json` do zwykłej Historii i Statystyk przy pierwszym uruchomieniu. Zachowuje SBH jako oddzielne pole danych, nie używa go jako TOTAL TIME. Dane pozostają lokalnie na urządzeniu.

Wgraj wszystkie pliki z tego folderu do root repozytorium GitHub Pages. Po aktualizacji otwórz stronę w Safari i odśwież ją.


## Import lotów — wersja poprawiona
Przy pierwszym uruchomieniu tej wersji aplikacja zastępuje poprzednią, niepełną bazę lotów wpisami odczytanymi z arkuszy rocznych 2018–2026. Import nie jest ponawiany przy kolejnych uruchomieniach, aby zachować późniejsze edycje. `TOTAL TIME` jest źródłem pola czasu lotu; `SBH` pozostaje osobnym polem. W pliku źródłowym suma datowanych wierszy z czasem dodatnim wynosi 2177:18, natomiast podsumowanie widoczne w arkuszu pokazuje 2183:31 — ta różnica 6:13 wymaga osobnej weryfikacji w samym Excelu i nie jest sztucznie dopisywana.
