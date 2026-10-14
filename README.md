# Pilot Logbook v2.2.7 — PICUS role fix

Ta poprawka ustawia importowane odcinki z niepustym dowódcą innym niż SELF jako PICUS równy block time, ale nie zaznacza automatycznie PIC ani Co-pilot/SIC. To odzwierciedla przypadek, gdy użytkownik był PF jako PICUS, a formalnym dowódcą był inny pilot.

Przed aktualizacją wyeksportuj kopię JSON. Wgraj `index.html` i `sw.js` do głównego katalogu repozytorium GitHub, zastępując stare pliki, następnie Commit changes. Wersja aplikacji: v2.2.7.

Poprawka dotyczy nowych importów; nie zmienia automatycznie wpisów już zapisanych.
