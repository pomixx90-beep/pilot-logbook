POMIWO logbook v2.2.47 — synchronizacja dwukierunkowa przez Google Sheets

WAŻNE: przed wdrożeniem wyeksportuj kopię JSON z KOMPUTERA i iPHONA.

1. Rozpakuj ZIP. W GitHubie zastąp index.html, sw.js i manifest.json plikami z paczki. Nie usuwaj ani nie nadpisuj workbook-data.json.
2. W Google Cloud klient OAuth musi mieć autoryzowane źródło JavaScript: https://pomixx90-beep.github.io. Używany jest Client ID wpisany w index.html; Client Secret nie jest używany.
3. W ekranie zgody OAuth dodaj swoje konto jako użytkownika testowego. Google Sheets API musi być włączone.
4. Otwórz aplikację na pierwszym urządzeniu → Dane i kopie zapasowe → „Połącz Google Sheets / synchronizuj”. Zaloguj się kontem mającym dostęp do arkusza i zaakceptuj uprawnienie do odczytu i zapisu arkuszy.
5. Powtórz logowanie na drugim urządzeniu. Oba urządzenia muszą być połączone tym samym kontem Google i mieć otwartą aplikację; synchronizacja sprawdza zmiany co 60 sekund i po zapisie lotu.
6. Aplikacja utworzy w istniejącym arkuszu kartę LogbookSync. Nie kasuj tej karty — przechowuje współdzielone wpisy jako JSON. Karta Flights nadal jest źródłem lotów mailowych.

Sesja OAuth jest przechowywana tylko w pamięci aplikacji. Gdy aplikacja pozostaje otwarta, synchronizacja działa co minutę, a odnowienie tokenu próbuje przebiec bez wymuszania okna wyboru konta. Po zamknięciu/ponownym otwarciu aplikacji może być konieczne ponowne połączenie.

Ograniczenia tej wersji: synchronizuje nowe wpisy i łączy istniejące bez zastępowania historii. Edycje istniejących lotów i usunięcia nie są jeszcze rozsyłane między urządzeniami. Jeśli Google zgłosi brak uprawnień, kliknij ponownie „Połącz Google Sheets / synchronizuj” i zaakceptuj nowe uprawnienie.

Nie udostępniaj Client Secret ani nie umieszczaj go w repozytorium. Zachowaj kopie JSON obu urządzeń do czasu potwierdzenia poprawnego działania.
