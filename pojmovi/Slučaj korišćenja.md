---
tip: pojam
aliases: [use case, primena]
izvor: "ISO/IEC TR 24030:2024, Artificial intelligence (AI) - Use cases, odeljak 6.4 (šablon slučaja korišćenja: ciljevi 6.4.6, ključni pokazatelji uspeha 6.4.10)"
---
# Slučaj korišćenja (use case)

## Definicija
Slučaj korišćenja je upotreba [[AI tehnologija|AI tehnologije]] u određenom kontekstu radi ostvarenja cilja, sa zadatim [[Ograničenje|ograničenjima]] i [[Metrika uspeha|metrikama uspeha]].

## Primer
Fabrika [[Orion Precizni Delovi]] ima tri slučaja korišćenja:
- **Nacrt radne instrukcije** (generisanje sadržaja): tehnolog dobija od jezičkog modela nacrt instrukcije za novi deo. Ograničenje je da tehnolog ima ograničeno vreme za pregled, a metrika uspeha je činjenična ispravnost nacrta prema tehničkoj dokumentaciji.
- **Vizuelna kontrola delova** (analiza sadržaja): kamere nad izlaznom trakom otkrivaju defekte i prijavljuju ih kontroloru kvaliteta. Ograničenje je da kontrolor može da proveri ograničen broj upozorenja po smeni, a metrika uspeha su odziv na retke defekte i preciznost upozorenja.
- **Prediktivno održavanje vretena** (odlučivanje): cilj je da se vreteno mašine CNC-07 zameni pre otkaza, bez nepotrebnih zamena. Ograničenje je da za taj tip vretena postoji samo jedno rezervno vreteno, a metrika uspeha je ukupan trošak ugovorne kazne, oštećenja alata i preuranjene zamene.

## Napomene
- Kontekst (Orion, Lipa) nije slučaj korišćenja. Kontekst je okruženje koje sadrži više slučajeva korišćenja.
- Jedan slučaj korišćenja može koristiti više vrsta AI tehnologije, na primer analizu i odlučivanje.
- [[Problem|Problemi]] se uvek javljaju u nekom slučaju korišćenja, jer tek tamo ograničenja i metrike uspeha kažu šta je neželjeno.
- Blisko je pojmu use case iz softverskog inženjerstva, ali ovde je u središtu cilj upotrebe tehnologije, sa ograničenjima i metrikama, a ne tok interakcije korisnika i sistema.
