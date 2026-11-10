---
tip: pojam
aliases: [constraint]
izvor: "Boyd i Vandenberghe, Convex Optimization (2004), poglavlje o optimizacionim problemima"
---
# Ograničenje (constraint)

## Definicija
Ograničenje je uslov [[Slučaj korišćenja|slučaja korišćenja]] koji određuje koje alternative (ili izlazi AI tehnologije) su dozvoljene. Tvrdo ograničenje se ne sme prekršiti: alternativa koja ga krši nije dozvoljena za izbor u [[Odluka|odluci]]. Meko ograničenje se sme prekršiti uz cenu. Alternative koje zadovoljavaju sva tvrda ograničenja čine skup dozvoljenih alternativa.

## Primer
U slučaju korišćenja "Prediktivno održavanje vretena" u fabrici [[Orion Precizni Delovi]] ograničenje je da u skladištu postoji samo jedno rezervno vreteno za taj tip. Mašine CNC-07 i CNC-09 imaju vretena istog tipa, pa alternativa "zameniti vretena na obe mašine odmah" nije dozvoljena (tvrdo ograničenje). Drugo tvrdo ograničenje je sertifikat: operater mora imati sertifikat za tip mašine, a u drugoj smeni radi samo jedan operater sa sertifikatom za taj tip, pa raspored u kome CNC-07 i CNC-09 u drugoj smeni rade istovremeno nije dozvoljen. Rok isporuke naloga N-2417 je meko ograničenje: kašnjenje je dozvoljeno, ali se ugovorno naplaćuje sa 200 EUR po danu.

## Napomene
- Ograničenje odgovara na pitanje šta mora da važi, a [[Metrika uspeha|metrika uspeha]] na pitanje koliko je dobro ostvaren cilj. [[Greška|Greška]] je izlaz koji narušava ograničenje ili metriku uspeha.
- Razlikuju se tvrda ograničenja, koja se ne smeju prekršiti (sertifikat operatera), i meka, čije je kršenje dozvoljeno uz cenu. Rok isporuke je meko ograničenje ako se kašnjenje ugovorno naplaćuje, pa se kazna unosi u [[Funkcija cilja|funkciju cilja]].
- Engleski *limitation* (ograničenje tehnologije) nije ovaj pojam. To je [[Nedostatak|nedostatak]] AI tehnologije.
