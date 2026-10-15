# Pilot Logbook v2.2.37 — poprawka BLOCK z maila i SBH w Historii

- Jeśli lot z Excela ma BLOCK równy 0, a dopasowany lot z importu mailowego ma poprawny BLOCK obliczony z OnBlock − OffBlock, aplikacja zachowuje wartość z maila.
- Loty z Excela nie pokazują już indywidualnego kafelka SBH, aby suma SBH dnia nie była powielona przy jednym z sektorów. Suma pozostaje w nagłówku grupy dnia.
- Dla wpisów wyłącznie mailowych indywidualny SBH nadal jest widoczny, a nagłówek pokazuje sumę dnia.
- Wersja importu Excela zwiększona do 23, aby wymusić ponowne zbudowanie i scalenie lokalnych danych.

## Wdrożenie
1. Zrób eksport JSON z aplikacji jako kopię bezpieczeństwa.
2. Podmień w GitHub tylko `index.html` i `sw.js`. Nie podmieniaj `workbook-data.json`.
3. Zapisz zmiany, poczekaj na publikację i sprawdź wersję v2.2.37.
4. Po uruchomieniu sprawdź daty 2026-10-13 i 2026-10-11.

Składnia JavaScript sprawdzona. Nie mam dostępu do lokalnej bazy przeglądarki, więc wynik należy potwierdzić po wdrożeniu.
