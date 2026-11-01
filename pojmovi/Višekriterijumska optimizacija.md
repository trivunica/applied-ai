---
tip: pojam
aliases: [multi-objective optimization, multicriteria optimization, kompromis]
izvor: "Miettinen, Nonlinear Multiobjective Optimization (1999)"
---
# Višekriterijumska optimizacija (multi-objective optimization)

## Definicija
[[Optimizacija]] sa dve ili više [[Funkcija cilja|funkcija cilja]] koje su u sukobu, tako da ne postoji alternativa koja je najbolja po svim funkcijama istovremeno. Rešenje je skup kompromisnih alternativa od kojih se nijedna ne može poboljšati po jednoj funkciji cilja bez pogoršanja po bar jednoj drugoj (Pareto-optimalne alternative).

## Primer
Planer u fabrici [[Orion Precizni Delovi]] želi da istovremeno minimizuje ukupnu ugovornu kaznu i nedeljnu potrošnju električne energije, koja se zbog vršne potrošnje dodatno naplaćuje. Tri rasporeda daju: R1 kaznu 400 EUR i 15.200 kWh, R2 kaznu 700 EUR i 14.400 kWh, R3 kaznu 900 EUR i 14.600 kWh. R3 je gori od R2 po oba kriterijuma, pa otpada. R1 i R2 su Pareto-optimalni: nijedan nije bolji od drugog po oba kriterijuma. Između njih odlučuje planer, jer optimizacija ne kaže koliko vredi 300 EUR kazne naspram 800 kWh.

## Napomene
- U svakodnevnom govoru ovaj problem se opisuje kao traženje kompromisa, na primer manji trošak naspram većeg kvaliteta.
- Izbor jedne alternative iz skupa kompromisnih traži dodatnu informaciju o prioritetima donosioca odluke, na primer težine kriterijuma ili [[Funkcija korisnosti|funkciju korisnosti]]. To nije deo same optimizacije.
- Blisko je višekriterijumskom odlučivanju, koje obuhvata i izbor među unapred zadatim alternativama.
