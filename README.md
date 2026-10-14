# Pilot Logbook v2.2.13 — PICUS/SIC fix

Ta wersja rozdziela PICUS od SIC/Co-pilot. Dla importowanych lotów Verified Flights, gdzie Crew Code pasuje do TakeOffPilot, a dowódca jest inny niż SELF, zapisuje PICUS równy block time, ale SIC = 0 i Co-pilot pozostaje odznaczony.

Przy starcie aplikacji poprawia również istniejące wpisy Imported from Verified Flights z PICUS > 0: zeruje SIC i odznacza Co-pilot, bez modyfikowania innych lotów.

Wdrożenie: zrób kopię JSON, następnie zastąp index.html i sw.js w głównym katalogu repozytorium GitHub i zatwierdź zmiany.
