# Pilot Logbook v2.2.36 — naprawa duplikatów i SBH dnia

W tej wersji:
- wpisy z importu mailowego dopasowane do lotów z Excela (ta sama data, trasa i rejestracja) są scalane zamiast wyświetlane jako duplikaty;
- zachowane zostają numer lotu i identyfikator źródłowy z maila;
- czas BLOCK i SBH z Excela pozostają wartościami nadrzędnymi;
- loty występujące tylko w imporcie mailowym pozostają w historii, a ich SBH nadal sumuje się na poziomie dnia;
- odświeżenie danych wymusza ponowny import `workbook-data.json` (import version 22).

## Wdrożenie
1. Zrób kopię JSON z aplikacji.
2. W GitHub podmień `index.html`, `sw.js` oraz `workbook-data.json` z tej paczki.
3. Zapisz zmiany i poczekaj na publikację.
4. Sprawdź wersję `v2.2.36`, a następnie dzień 2026-10-11 i 2026-10-13.

Uwaga: dopasowanie łączy rekordy z identyczną datą, trasą i rejestracją. Jeśli masz dwa rzeczywiście różne loty na tej samej trasie, tego samego dnia i tym samym samolotem, sprawdź je po wdrożeniu.
