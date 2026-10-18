POMIWO logbook v2.2.53 — poprawka sesji Google

Zmiany:
- Po otwarciu aplikacja próbuje wznowić sesję Google bez ponownego wymuszania ekranu zgody.
- Przycisk synchronizacji najpierw wykorzystuje istniejącą zgodę; interaktywna zgoda jest uruchamiana tylko, gdy jest potrzebna.
- Token OAuth pozostaje w pamięci aplikacji, nie jest zapisywany na stałe.

Wdrożenie:
1. Zrób kopię JSON lotów.
2. Podmień index.html i sw.js w repozytorium GitHub Pages.
3. Zapisz zmiany i poczekaj na publikację.
4. Otwórz aplikację i kliknij „Odśwież aplikację”.
5. Jeśli Google wymaga nowej zgody, kliknij „Połącz Google Sheets / synchronizuj” i zaakceptuj dostęp.

Wznowienie bez interakcji działa, jeśli Google nadal pamięta wcześniejszą zgodę i domena jest poprawnie skonfigurowana w OAuth. Nie wykonano rzeczywistej synchronizacji z kontem Google.
