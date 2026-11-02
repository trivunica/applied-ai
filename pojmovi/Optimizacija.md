---
tip: pojam
aliases: [optimization]
izvor: "Boyd i Vandenberghe, Convex Optimization (2004), poglavlje o optimizacionim problemima"
---
# Optimizacija (optimization)

## Definicija
Postupak izbora alternative koja minimizuje ili maksimizuje [[Funkcija cilja|funkciju cilja]] među alternativama koje zadovoljavaju sva [[Ograničenje|ograničenja]].

## Primer
Planer u fabrici [[Orion Precizni Delovi]] koristi softver koji za nedeljne naloge i 12 mašina traži raspored sa najmanjom ukupnom ugovornom kaznom. Softver ne razmatra rasporede koji krše ograničenja (jedan nalog po mašini, sertifikati operatera, trajanje smene) i vraća raspored sa kaznom od 400 EUR.

## Napomene
- Rešenje je optimalno samo u odnosu na zadatu funkciju cilja i ograničenja. Ako ona loše opisuju stvarni problem, optimalno rešenje može biti loše u praksi.
- Postupak ne mora da garantuje najbolje rešenje. Za velike probleme koriste se heuristike koje daju dovoljno dobro rešenje u razumnom vremenu.
- Pojam se koristi i pri treniranju modela, gde se optimizuju parametri modela. Ovde se misli na izbor alternative u odluci.
