# Pilot Logbook v2.2.41 — naprawa aktualizacji BLOCK z Verified Flights

Ta poprawka bazuje na plikach aplikacji i eksporcie JSON przesłanych 15.10.2026.

## Przyczyna
W imporcie BLOCK był liczony najpierw z OnBlock − OffBlock. Jeśli te wartości nie zostały rozpoznane w danym eksporcie, zapasowy `TotalBlock` był parsowany przez funkcję akceptującą wyłącznie `H:MM`, podczas gdy arkusz może przekazać czas w formacie `H:MM:SS`. Wtedy BLOCK pozostawał równy 0. Istniejące rekordy mają `sourceId`, ale nie mają zapisanej wartości `block`.

## Zmiana
- `BLOCK` nadal jest liczony przede wszystkim jako `OnBlock − OffBlock`, z obsługą północy.
- `TotalBlock` jest teraz poprawnie parsowany jako zapas, również w formacie `H:MM:SS`.
- Gdy istniejący lot zostaje dopasowany, poprawiony BLOCK jest zapisywany do istniejącego wpisu, bez tworzenia duplikatu.
- Komunikat po imporcie informuje o aktualizacji istniejących wpisów, nie tylko SBH.
- Zmieniono wersję aplikacji i cache na v2.2.41.

## Wdrożenie
1. Wyeksportuj aktualną kopię JSON.
2. W repozytorium GitHub podmień tylko `index.html` i `sw.js`.
3. Nie podmieniaj `workbook-data.json` — zachowaj bieżący test bez lotów z 13.10.2026.
4. Otwórz Import / eksport i ponownie zaimportuj `Pilot Logbook - Verified Flights Inbox.xlsx`.
5. Po imporcie komunikat powinien podać liczbę zaktualizowanych istniejących wpisów. Dla 13.10.2026 oczekiwane BLOCK: FR2143P 1:24, FR2749 2:05, FR2750 1:04, FR7950 2:05, FR7951 1:38.

Jeśli liczba zaktualizowanych wpisów wyniesie 0, nie czyść danych. Zachowaj komunikat z importu i wyeksportuj JSON ponownie do diagnostyki.
