POMIWO logbook v2.2.45 — Google Sheets sync (read-only)

1. Przed aktualizacją wyeksportuj kopię JSON z aplikacji na każdym urządzeniu.
2. W repozytorium GitHub zastąp index.html i sw.js; pozostaw workbook-data.json bez zmian. manifest.json również można zastąpić plikiem z paczki.
3. Ustawienia OAuth: klient Web musi mieć autoryzowane źródło JavaScript https://pomixx90-beep.github.io. Klient ID jest wpisany w index.html; Client Secret nie jest używany.
4. Google Sheets API musi być włączone, a konto Google dodane jako użytkownik testowy na ekranie zgody OAuth.
5. W aplikacji otwórz Dane i kopie zapasowe → „Połącz Google Sheets / synchronizuj”, zaloguj się tym samym kontem, które ma dostęp do arkusza.
6. Aplikacja odczytuje kartę Flights z arkusza wskazanego w konfiguracji, dodaje nowe loty do lokalnej historii i pomija duplikaty. Nie wysyła lokalnych wpisów do Google Sheets; jest to synchronizacja jednokierunkowa z arkusza do urządzenia.

Uwaga: ten pakiet nie zawiera workbook-data.json. Nie usuwaj istniejącego pliku danych ani nie nadpisuj lokalnej historii.
