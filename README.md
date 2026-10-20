POMIWO Logbook v2.2.82 — Finance live calculations

Zmiany w sekcji Finanse:
- SBH miesięczne jest sumowane z lotów zapisanych w aplikacji (sectorSBH, a w razie braku sbh).
- Stawki, kredyt/rata, workoff days (200 EUR/dzień), safety pilot (godziny) oraz ZUS/koszty można edytować osobno dla każdego miesiąca. Te ustawienia zapisują się lokalnie w przeglądarce.
- SBH roczny lub miesięczny można ręcznie nadpisać tylko do podglądu; nie jest zapisywany.
- Kurs EUR/PLN jest pobierany z publicznego API NBP (tabela A). Gdy API jest niedostępne, używany jest kurs zapasowy z istniejących danych źródłowych. Kurs można ręcznie zmienić dla bieżącego podglądu.
- Widok miesięcy to responsywne karty zamiast szerokiej, przewijanej tabeli.

Uwaga: ustawienia finansowe są przechowywane lokalnie na tym urządzeniu/przeglądarce. Ręczny SBH jest tymczasowy i znika po przeładowaniu aplikacji. Kalkulacje są szacunkowe i nie stanowią księgowego rozliczenia podatkowego.


Finance v2.2.83: added editable monthly ryczałt percentage (default 8.5%) and VAT percentage (default 23%), with monthly and yearly PLN totals. Tax/VAT calculations follow the original Invoice sheet structure: ryczałt on gross EUR converted to PLN; VAT as percentage of gross EUR converted to PLN. Estimated payout subtracts ryczałt and ZUS, as in the workbook payout formula; VAT is displayed separately. Verify with accountant before relying on tax estimates.
