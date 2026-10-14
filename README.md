# Pilot Logbook PWA — wersja na iPhone'a

To jest prototyp aplikacji webowej offline-first. Zawiera dodawanie/edycję/usuwanie lotów, statystyki, wskaźniki czasu lotu, import CSV z Excela oraz eksport CSV i kopii JSON.

## Ważne ograniczenie
Dane są przechowywane lokalnie w przeglądarce. Automatyczna synchronizacja z chmurą między urządzeniami nie jest włączona, bo wymaga hostingu HTTPS i skonfigurowanego backendu/autoryzacji. Nie należy traktować kopii lokalnej jako jedynej kopii danych.

## Uruchomienie na iPhonie
Do instalacji jako PWA pliki muszą być udostępnione przez adres HTTPS. Samo otwarcie pliku HTML z aplikacji Pliki nie wystarczy do instalacji PWA ani działania service workera.
1. Umieść zawartość tego folderu na hostingu HTTPS obsługującym pliki statyczne.
2. Otwórz adres w Safari na iPhonie.
3. Naciśnij Udostępnij → Dodaj do ekranu początkowego.
4. Uruchom ikonę Pilot Logbook.
5. Przed dodawaniem prawdziwych danych przetestuj eksport JSON i kopię zapasową.

## Import CSV
W Excelu wybierz Zapisz jako → CSV UTF-8. Oczekiwane nagłówki m.in.:
Date, Flight Number, Aircraft Type, Registration, Departure, Arrival, Block Time, PIC, SIC, IFR, Night, Landings, Notes
Daty: yyyy-MM-dd lub dd.MM.yyyy. Czas: HH:MM lub liczba godzin dziesiętnie.

## EASA / FTL
Wskaźniki 100:00/28 dni i 900:00/365 dni są prostymi sumami wpisanego block time. Nie są kompletną kontrolą zgodności FTL. Do zastosowania operacyjnego potrzebna jest walidacja wobec aktualnych przepisów oraz zatwierdzonego schematu operatora.
