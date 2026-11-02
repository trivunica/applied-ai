---
tip: pojam
aliases: [constraint]
izvor: "Boyd i Vandenberghe, Convex Optimization (2004), poglavlje o optimizacionim problemima"
---
# Ograničenje (constraint)

## Definicija
Uslov koji alternativa mora da zadovolji da bi bila dozvoljena za izbor u [[Odluka|odluci]]. Alternative koje zadovoljavaju sva ograničenja čine skup dozvoljenih alternativa.

## Primer
Pri nedeljnom planiranju u fabrici [[Orion Precizni Delovi]] važe tri ograničenja: mašina obrađuje najviše jedan nalog istovremeno, smena traje 8 sati, i operater mora imati sertifikat za tip mašine. Raspored u kome se N-2417 i N-2418 u drugoj smeni istovremeno obrađuju na mašinama CNC-07 i CNC-09 nije dozvoljen, jer obe mašine zahtevaju operatera sa sertifikatom za taj tip, a u drugoj smeni radi samo jedan takav operater.

## Napomene
- Razlikuju se tvrda ograničenja, koja se ne smeju prekršiti (sertifikat operatera), i meka, čije je kršenje dozvoljeno uz cenu. Rok isporuke naloga je meko ograničenje ako se kašnjenje ugovorno naplaćuje, pa se kazna unosi u [[Funkcija cilja|funkciju cilja]].
