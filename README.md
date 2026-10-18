POMIWO Logbook v2.2.67

Naprawy:
- Usunięto specjalny filtr odrzucający loty z 2026-10-13 przy odczycie LogbookSync.
- Usunięto czyszczenie lokalnych wpisów z 2026-10-13 podczas importu Excela. Brak lotów w JSON oznacza tylko brak bazowych wpisów Excelowych, a nie zakaz importu z e-maila.
- Podniesiono importVersion i cache key, aby uruchomić przebudowę danych.

Statystyki źródłowe wymagają dalszej weryfikacji na Twoim rzeczywistym stanie danych: osadzony JSON ma 964 rekordy, sumę BLOCK 129719 min (2151:59), podczas gdy metadane wskazują expectedSourceTotalMinutes=131011 i importedRowsTotalMinutes=130638. To rozbieżność już w danych źródłowych/konwersji i nie należy jej maskować stałą korektą.

Rozpakuj do nowego folderu i otwórz index.html. Wpisy z e-maila z 13.10 mogą być importowane nawet jeśli JSON Excela nie zawiera tej daty.
