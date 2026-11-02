---
tip: pojam
aliases: [prediction]
izvor: "ISO/IEC 22989:2022, Information technology - Artificial intelligence - AI concepts and terminology"
---
# Predikcija (prediction)

## Definicija
Procena vrednosti ili ishoda koji nije poznat u trenutku odlučivanja, koju [[Model|model]] izračunava iz podataka.

## Primer
Iz [[Vremenska serija|vremenske serije]] vibracija vretena mašine CNC-07 model u fabrici [[Orion Precizni Delovi]] procenjuje da će vreteno otkazati u narednih deset dana sa verovatnoćom 30%. Procena nije odluka: rukovodilac održavanja na osnovu nje tek bira šta će uraditi.

## Napomene
- Predikcija se ne odnosi samo na budućnost. Kamere na liniji vizuelne kontrole predviđaju da li je deo ispravan, što je trenutno nepoznato svojstvo dela koje već postoji.
- Predikcija je ulaz u [[Odluka|odluku]], ali nije svaka odluka zasnovana na predikciji.
- Broj koji model vrati (na primer 85%) ne mora biti prava verovatnoća. Ako model nije kalibrisan, 85% ne znači da se u 85 od 100 takvih slučajeva ishod zaista dogodi.
- Svaka predikcija nosi [[Neizvesnost|neizvesnost]].
