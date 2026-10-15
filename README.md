# Pilot Logbook v2.2.33 — SBH w Historii

Zmiany:
- W Historii po prawej stronie od kafelka BLOCK dodany jest żółty kafelek SBH.
- Dla wpisów z logbooka zachowywany jest zapisany czas SBH (w tym wartości z arkusza od 2025 r.).
- Przy imporcie Verified Flights SBH jest wyliczany jako różnica STA − STD, z obsługą przejścia przez północ.
- Podczas kolejnego importu istniejące wpisy, które wcześniej nie miały SBH, są uzupełniane na podstawie STA/STD zamiast być tylko pomijane jako duplikaty.
- Zmieniono wersję aplikacji i klucz cache service workera.

## Wdrożenie
1. Wyeksportuj kopię JSON z aplikacji.
2. W repozytorium GitHub podmień tylko `index.html` i `sw.js`. Nie podmieniaj `workbook-data.json` dla tej zmiany.
3. Zapisz commit i odśwież aplikację. Powinna pokazywać v2.2.33.
4. Przy imporcie Verified Flights wybierz arkusz zawierający kolumny `STD` i `STA`; istniejące wpisy zostaną uzupełnione, jeśli SBH było puste.

Kontrola: sprawdzono składnię JavaScript przez `node --check`. Nie wykonano rzeczywistego importu z konta Google ani testu w urządzeniu użytkownika.


Historia v2.2.33: loty są grupowane według daty. Po prawej stronie grupy widoczny jest żółty łączny SBH dnia, a żółta klamra wizualnie obejmuje loty z tej daty. Dla Excela sumuje istniejące wpisy SBH z danego dnia; dla importu mailowego sumuje SBH poszczególnych sektorów (STA − STD).
