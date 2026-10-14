# Pilot Logbook PWA — iPhone

Pakiet zawiera aplikację Pilot Logbook oraz dane wczytane z przesłanego pliku `Logbook.xlsx`.

## Import danych z Excela
- Przy pierwszym uruchomieniu aplikacja automatycznie wczytuje `workbook-data.json` i zapisuje kopię w lokalnej pamięci przeglądarki.
- Zakładka **Arkusze Excel** pokazuje wszystkie arkusze z pliku, także ukryte, wraz z wierszami i kolumnami. Można wybrać zakładkę, wyszukiwać tekst i wyeksportować dane do JSON.
- Nazwy arkuszy i układ kolumn są zachowane. Komórki z formułami są przechowywane jako tekst formuły, a formuły nie są przeliczane przez aplikację.
- To import jednorazowy z kopii pliku. Zmiany w późniejszej wersji pliku Excel nie pojawią się automatycznie — trzeba przygotować nowy pakiet z aktualnym plikiem.

## Instalacja na iPhonie
1. Umieść wszystkie pliki z folderu na hostingu HTTPS (np. w repozytorium GitHub Pages), nie tylko `index.html`.
2. Otwórz stronę w Safari.
3. Wybierz **Udostępnij → Dodaj do ekranu początkowego**.
4. Otwórz aplikację z ikony. Przy pierwszym uruchomieniu wymagane jest połączenie z internetem, aby pobrać pakiet danych; potem pliki aplikacji są buforowane do pracy offline.

## Przechowywanie
Dane są zapisane lokalnie na urządzeniu. Nie są wysyłane do serwera. Wyczyść dane witryny tylko po wykonaniu kopii zapasowej.
