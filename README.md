POMIWO Logbook v2.2.81 — sekcja Finanse

W paczce są pliki aplikacji oraz finance-data.enc.json. Arkusz Invoice został usunięty z publicznego workbook-data.json i z osadzonej kopii w index.html. Dane finansowe są osobno szyfrowane AES-256-GCM; klucz uzyskiwany jest w przeglądarce z hasła przez PBKDF2-SHA256 (310 000 iteracji). Hasło nie jest zapisane w plikach aplikacji. Dane odszyfrowane nie są zapisywane do localStorage ani IndexedDB, a sekcja blokuje się po przejściu do innej karty, ukryciu aplikacji lub 5 minutach bezczynności.

WDROŻENIE: wgraj wszystkie pliki z katalogu POMIWO_logbook_v2.2.81_FINANCE_LOCKED do głównego katalogu hostingu, nadpisując index.html, workbook-data.json, sw.js i manifest.json. Nie pomijaj finance-data.enc.json. Następnie otwórz aplikację online i potwierdź, że wersja to v2.2.81.

Uwaga bezpieczeństwa: to ochrona danych szyfrowaniem po stronie klienta, nie kontrola dostępu na poziomie serwera. Plik zaszyfrowany jest publicznie pobieralny, ale nie zawiera jawnych wartości. Każdy, kto zna hasło, może go odszyfrować.

