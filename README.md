# Pilot Logbook — aktualizacja statystyk

## Co się zmieniło
- Dodano wybór roku w sekcji „Statystyki roczne”.
- Statystyki miesięczne, typy samolotów, rejestracje, destynacje i czasy funkcji są liczone bezpośrednio z wpisów lotów dla wybranego roku.
- Usunięto statyczne wartości kopiowane z arkusza Excel „Statistic”.
- Zmieniono cache Service Workera na `pilot-logbook-v7`.
- Pozostawiono dotychczasowy klucz i wersję importu, aby aktualizacja kodu nie nadpisała lokalnych wpisów użytkownika.

## Aktualizacja na GitHub Pages z iPhone’a
1. Otwórz repozytorium `pomixx90-beep/pilot-logbook` na GitHubie.
2. Zastąp w katalogu głównym plik `index.html` nowym plikiem z tego ZIP-a.
3. Zastąp w katalogu głównym plik `sw.js` nowym plikiem z tego ZIP-a.
4. Zapisz zmiany/commit.
5. Po publikacji otwórz stronę ponownie. Jeśli widzisz starą wersję, zamknij kartę i otwórz stronę ponownie; nowy cache Service Workera ma nazwę `pilot-logbook-v7`.

Nie podmieniaj `workbook-data.json`, jeśli nie chcesz zmieniać przygotowanej bazy importu. Przed aktualizacją zachowaj kopię JSON z aplikacji.
