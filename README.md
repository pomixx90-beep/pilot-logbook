# Pilot Logbook v2.2.35 — BLOCK z OnBlock − OffBlock

Naprawia import Verified Flights z maila: BLOCK jest obliczany z `OnBlock - OffBlock`, z obsługą przejścia przez północ. Jeśli rekord został już wcześniej zaimportowany z `BLOCK 0:00`, ponowny import uzupełni jego czas zamiast pozostawić błędną wartość. Pole `TotalBlock` jest używane jako wartość zapasowa tylko wtedy, gdy nie da się obliczyć czasu z OnBlock/OffBlock.

## Wdrożenie
1. Wyeksportuj kopię JSON z aplikacji.
2. W GitHub podmień `index.html` i `sw.js`.
3. Zapisz zmiany, poczekaj na GitHub Pages i otwórz aplikację z wersją `v2.2.35`.
4. Ponownie zaimportuj plik Verified Flights. Import naprawi także istniejące duplikaty z zerowym lub niezgodnym BLOCK.

`workbook-data.json` nie wymaga podmiany.
