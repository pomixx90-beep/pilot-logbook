Pilot Logbook v2.2.39 — poprawka sumy SBH dnia

Zmiany:
- Gdy dla danego dnia istnieją wpisy połączone z importem Verified Flights, suma SBH dnia liczy tylko wartości SBH z wpisów mailowych (na poziomie sektorów), a nie dodaje do nich dziennej wartości SBH z Excela.
- Przy dopasowaniu maila do lotu z Excela zapisuje SBH z maila jako czas dla sektora. Dla dni bez importu mailowego pozostaje SBH z Excela.
- BLOCK z maila pozostaje obliczany jako OnBlock − OffBlock; nie zmieniano tego mechanizmu.

W GitHub podmień index.html i sw.js. Zrób kopię JSON przed aktualizacją. workbook-data.json nie jest potrzebny do tej poprawki.
