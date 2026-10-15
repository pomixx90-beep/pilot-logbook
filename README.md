# Pilot Logbook v2.2.38 — rebuild danych, statystyk i BLOCK

## Co zostało naprawione
- Dane roczne przebudowane z przesłanego `Logbook(2).xlsx`, z odczytem wartości wynikowych formuł.
- Potwierdzone korekty danych: `2022!A32` ustawione na `2022-06-10`; `2025!B169` zmienione z `LPDPL` na `LDPL`.
- Ponownie wyliczone pola PIC, Co-pilot/SIC, Dual, IFR, NIGHT, SE, ME, Multi-pilot, starty i lądowania na podstawie właściwych kolumn arkuszy.
- Import wersji podniesiony do 24, aby aplikacja ponownie załadowała dane źródłowe.
- Migracja łączy istniejące rekordy z importu mailowego z odpowiadającymi im lotami Excela, normalizując rejestrację (np. `SP-RSA` i `SPRSA`), aby uniknąć dubli.
- Parser czasu obsługuje wartości czasu oraz daty z godziną eksportowane z arkuszy.
- Import Verified Flights nadal wylicza BLOCK jako `OnBlock - OffBlock`, a przy duplikacie uzupełnia istniejący rekord.

## Kontrole przygotowanego JSON
- Loty z arkuszy: 977
- Czas blokowy: 2183:31
- PIC: 1003:00
- Co-pilot/SIC: 1092:10
- Dual: 87:37
- IFR: 1998:58
- NIGHT: 527:52
- SE: 169:28
- ME: 2014:03
- Multi-pilot: 1983:19
- Starty dzień/noc: 941 / 217
- Lądowania dzień/noc: 885 / 273
- SBH dla 11.10.2026: 8:20

## Wdrożenie
1. Zrób kopię JSON z aplikacji.
2. Rozpakuj ZIP.
3. W repozytorium GitHub podmień `index.html`, `sw.js` i `workbook-data.json`.
4. Zapisz zmiany i zaczekaj na publikację GitHub Pages.
5. Sprawdź wersję `v2.2.38`. Po wdrożeniu sprawdź dashboard oraz BLOCK dla wcześniej zaimportowanych lotów mailowych.

Uwaga: pliki i składnię JavaScript sprawdzono lokalnie; nie wykonano testu w działającej przeglądarce ani na lokalnej bazie użytkownika.
