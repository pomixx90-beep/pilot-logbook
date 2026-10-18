POMIWO Logbook v2.2.66 — naprawa utraty sektorów i statystyk

Ustalona przyczyna: dedupeLocalFlights() używało dopasowania semantycznego także między dwoma rekordami z sourceSheet (oba z Excela). To mogło sklejać niezależne wiersze Excela i zaniżać liczbę sektorów oraz nalot.

Poprawka: rekordy z Excela nie są już wzajemnie deduplikowane semantycznie. Dopasowanie nadal służy do połączenia rekordu Excel z odpowiadającym wpisem e-mailowym/lokalnym. Podbito importVersion do 31, aby wymusić przebudowę historii według poprawionej reguły. Osadzony JSON zachowany; 13.10.2026 pozostaje puste.

Rozpakuj cały ZIP do nowego folderu i otwórz index.html. Zrób kopię JSON przed wdrożeniem.
