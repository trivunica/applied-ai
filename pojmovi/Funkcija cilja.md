---
tip: pojam
aliases: [objective function, kriterijumska funkcija]
izvor: "Boyd i Vandenberghe, Convex Optimization (2004), poglavlje o optimizacionim problemima"
---
# Funkcija cilja (objective function)

## Definicija
Funkcija cilja je vrsta [[Metrika uspeha|metrike uspeha]] u [[Slučaj korišćenja|slučaju korišćenja]] u kome se odlučuje: funkcija koja svakoj alternativi koja zadovoljava [[Ograničenje|ograničenja]] dodeljuje broj kojim se izražava koliko dobro ostvaruje cilj [[Odluka|odluke]], tako da se bira alternativa sa najmanjom ili najvećom vrednošću te funkcije.

## Primer
U slučaju korišćenja "Prediktivno održavanje vretena" u fabrici [[Orion Precizni Delovi]] funkcija cilja je ukupan trošak, i on se minimizuje. U nju ulaze ugovorna kazna za N-2417 (200 EUR po danu kašnjenja), oštećenje alata pri otkazu (8.000 EUR) i trošak preuranjene zamene (1.900 EUR zbog neiskorišćenog veka starog vretena). Alternativa A, zamena vretena pre servisa, ima izvestan trošak: 2 dana kašnjenja (2 × 200 = 400 EUR) plus 1.900 EUR, ukupno 2.300 EUR. Alternativa B, nastavak rada do servisa, ima očekivani trošak: otkaz sa verovatnoćom 30% donosi 8.000 + 6 × 200 = 9.200 EUR, pa je očekivana vrednost 0,3 × 9.200 = 2.760 EUR. Vrednost funkcije cilja je 2.300 za A i 2.760 za B, pa se bira A.

## Napomene
- Izbor funkcije cilja je sadržajna odluka. Ono što nije u njoj ne utiče na izbor: u primeru se zastoj mašine iskazuje samo preko dana kašnjenja i ugovorne kazne, pa izgubljeni mašinski sati van kazne ne utiču na izbor između A i B.
- Pri verovatnoći otkaza od 25% obe alternative imaju istu vrednost (0,25 × 9.200 = 2.300), pa je to granica na kojoj se izbor menja.
- Ne mešati sa funkcijom gubitka (loss function) pri treniranju modela mašinskog učenja. Ona meri grešku modela na podacima, a ne kvalitet alternative u odluci.
