---
tip: pojam
aliases: [fallback, fallback procedure]
izvor: "NIST AI 100-1, Artificial Intelligence Risk Management Framework (AI RMF 1.0), funkcija MANAGE, potkategorija 2.4, https://doi.org/10.6028/NIST.AI.100-1"
---
# Rezervni postupak (fallback)

## Definicija
Rezervni postupak je [[Rešenje|rešenje]] kojim se oporavlja [[Slučaj korišćenja|slučaj korišćenja]]: unapred određen način rada bez AI tehnologije, ili sa njenom ograničenom ulogom, na koji se prelazi kada tehnologija ne radi, ne odgovori na vreme ili je njena [[Neizvesnost|neizvesnost]] prevelika. Posao se tako nastavlja uz poznat i prihvatljiv kvalitet.

## Primer
U fabrici [[Orion Precizni Delovi]] senzori vibracija na mašini CNC-07 prestanu da šalju očitavanja, pa sistem za prediktivno održavanje ne može da proceni verovatnoću otkaza. Unapred je dogovoreno da se tada vreteno održava kao pre uvođenja sistema: po planiranom servisu, uz dnevni pregled operatera. Slično, ako kamere linije za vizuelnu kontrolu ne rade, kontrolor kvaliteta ručno pregleda svaki deseti deo.

## Napomene
- Razlika od [[Ljudski nadzor|ljudskog nadzora]]: kod nadzora čovek proverava izlaz AI tehnologije, a kod rezervnog postupka se taj izlaz ne koristi.
- Okidač prelaska (koliko dugo nema odgovora, koja neizvesnost je prevelika) i način povratka moraju biti određeni unapred, a ne u trenutku kvara.
- Rezervni postupak je obično sporiji ili skuplji. Njegova cena ulazi u procenu [[Rizik|rizika]] uvođenja AI tehnologije.
- Kod agenata, rezervni postupak je odgovor na istek vremena alata ili na petlju koja se ne završava.
