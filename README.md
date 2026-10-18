# POMIWO Logbook v2.2.75 — mail BLOCK + persistence fix

Zmiany:
- Import z Verified Flights nie nadpisuje BLOCK w rekordzie z Excela wartością e-mail, jeśli BLOCK nie zgadza się z różnicą OffBlock–OnBlock (tolerancja 2 min).
- Ta sama walidacja działa podczas scalania z Google Sheets, żeby stara wartość chmurowa nie przywracała błędnego czasu.
- Podniesiono wersję cache Service Workera i numer importu danych, aby wymusić odświeżenie zasobów aplikacji.
- Zachowano istniejące reguły dopasowywania lotów i importu SBH.

Wdrożenie: zastąp pliki aplikacji zawartością tego archiwum. Jeśli aplikacja była zainstalowana jako PWA, otwórz ją online i użyj przycisku Odśwież aplikację, a następnie wykonaj synchronizację ponownie.
