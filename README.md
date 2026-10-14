# Pilot Logbook — raporty i lądowania

Zmiany w tej wersji:
- podsumowanie Dashboardu przeniesione do Raporty → Czas; Dashboard pokazuje ostatnie loty;
- trasy w obie strony łączone w jeden wiersz z osobnymi sektorami i czasami dla każdego kierunku;
- typ samolotu w ręcznym formularzu to lista Boeing 737-700 / 737-800 / 737-8200;
- lądowania dzień/noc wybierane checkboxami i zapisywane osobno; importowane wartości dzienne/nocne są zachowywane, gdy są dostępne;
- cache service workera zwiększony do nowej wersji.

Czas nocny: nie naliczam go automatycznie z samego off-block/on-block, bo nie są to dokładne czasy take-off/landing ani pozycja samolotu w trakcie lotu. Proponowany mechanizm opisano w odpowiedzi; obecnie pole Night pozostaje ręczne.

Przed podmianą plików wykonaj eksport JSON. W GitHub Pages zastąp index.html i sw.js; pozostaw workbook-data.json, manifest.json i ikony.


## Czas nocny — kalkulator lokalny

Formularz lotu zawiera przycisk „Wylicz czas nocny (szacunek)”. Kalkulator działa offline i wykorzystuje lokalną tabelę współrzędnych lotnisk oraz obliczenie wysokości Słońca; granicą nocy jest zmierzch cywilny (Słońce na wysokości -6°). Trasę przybliża odcinek wielkiego koła między lotniskiem wylotu i przylotu, a czas opiera na godzinach off-block/on-block UTC. To tylko szacunek: block time obejmuje kołowanie, a rzeczywiste czasy startu/lądowania i przebieg trasy mogą się różnić. Użytkownik może ręcznie poprawić pole „Noc”. Jeśli kodu ICAO nie ma w lokalnej tabeli, kalkulator poprosi o ręczne wpisanie wartości.


## v1.7
- Naprawione ponowne wyliczanie block time, PIC/Co-pilot/Dual/Instructor oraz PICUS przy zmianie czasu, nazwiska i funkcji oraz przy zapisie.
- Dodane widoczne listy wyboru lotnisk z lotnisk występujących w poprzednich lotach i lokalnej listy współrzędnych. Można nadal wpisać kod ICAO ręcznie.
- Zmieniona nazwa cache Service Workera.


## v2.0 — naprawa danych raportów
- Zwiększono wersję importu Excela do 9, aby naprawić wcześniej zaimportowane rekordy bez NAME PIC i czasów funkcji.
- Mapowanie kolumn jest ustalane na podstawie nagłówków arkusza; poprawiono kolumnę lądowań nocnych.
- PICUS jest przeliczany na podstawie NAME PIC i block time przy migracji danych.
- Zmieniono cache Service Workera.
