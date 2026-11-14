---
tip: pojam
aliases: [model monitoring, post-deployment monitoring]
izvor: "NIST AI 100-1, Artificial Intelligence Risk Management Framework (AI RMF 1.0), funkcija MANAGE, potkategorija 4.1, https://doi.org/10.6028/NIST.AI.100-1"
---
# Praćenje modela u radu (model monitoring)

## Definicija
Praćenje modela u radu je vrsta [[Evaluacija|evaluacije]] koja se odvija neprekidno posle puštanja AI tehnologije u upotrebu: merenje njenih ulaza, izlaza i, kad su poznati, stvarnih ishoda, da bi se otkrilo kada [[Metrika uspeha|metrike uspeha]] počnu da opadaju.

## Primer
Fabrika [[Orion Precizni Delovi]] prelazi na novog dobavljača čelika, a posle toga vibracije vretena pri obradi su u proseku nešto jače. Praćenje uočava da se raspodela očitavanja vibracija pomerila u odnosu na podatke za treniranje i da sistem za prediktivno održavanje za tri nedelje izdaje dvostruko više upozorenja, iako u evidenciji nema više otkaza. Rukovodilac održavanja dobija izveštaj pre nego što počne da ignoriše upozorenja.

## Napomene
- Ishod (da li je vreteno stvarno otkazalo) često se sazna tek posle nekoliko dana ili nedelja. Zato se prate i ulazi i izlazi, koji se vide odmah.
- Praćenje otkriva [[Promena raspodele podataka|promenu raspodele podataka]], ali je ne ispravlja. Ispravka je [[Ponovno treniranje|ponovno treniranje]] ili [[Rezervni postupak|rezervni postupak]].
- Razlika od praćenja agenta (tracing): ovde se prati kvalitet modela kroz nedelje i mesece, a ne tok izvršavanja jednog zadatka.
