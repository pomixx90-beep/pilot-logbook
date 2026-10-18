POMIWO Logbook v2.2.68 — poprawka SBH

Naprawa: SBH z Excela jest dzienną wartością zapisaną przy jednym sektorze. Nie jest już nadpisywane przez SBH liczone z maila jako STA−STD, gdy aktualizowany rekord pochodzi z Excela. Mail nadal aktualizuje inne pola, w tym numer lotu i block. SBH dla wpisów mailowych bez odpowiednika w Excelu nadal jest liczone z STA−STD.

Wersja importu podniesiona do 33, by odbudować historię z osadzonego JSON-a. JSON i pusty dzień 13.10 są zachowane.

Uwaga: nie wprowadzono sztucznej korekty nalotu. Po wdrożeniu porównaj nalot całkowity z ręcznym logbookiem; rozbieżność 2:21 wymaga osobnego wskazania rekordów, których block różni się między Excelem i importem e-mail.
