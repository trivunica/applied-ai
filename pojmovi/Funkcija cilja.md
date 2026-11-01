---
tip: pojam
aliases: [objective function, kriterijumska funkcija]
izvor: "Boyd i Vandenberghe, Convex Optimization (2004), poglavlje o optimizacionim problemima"
---
# Funkcija cilja (objective function)

## Definicija
Funkcija koja svakoj alternativi koja zadovoljava [[Ograničenje|ograničenja]] dodeljuje broj kojim se izražava koliko dobro ostvaruje cilj [[Odluka|odluke]], tako da se bira alternativa sa najmanjom ili najvećom vrednošću te funkcije.

## Primer
Planer u fabrici [[Orion Precizni Delovi]] raspoređuje naloge po mašinama. Funkcija cilja je ukupna ugovorna kazna: za svaki nalog broj dana kašnjenja pomnožen dnevnom kaznom, sabrano po svim nalozima, i ona se minimizuje. Raspored A daje N-2417 kašnjenje od dva dana (2 × 200 EUR = 400 EUR). Raspored B ne kasni sa N-2417, ali N-2420 kasni jedan dan (1 × 500 EUR = 500 EUR). Vrednost funkcije cilja je 400 za A i 500 za B, pa planer bira A.

## Napomene
- Izbor funkcije cilja je sadržajna odluka. Ono što nije u njoj ne utiče na izbor: u primeru, raspored A ne razlikuje se od B po potrošnji energije jer energija nije uračunata.
- Ne mešati sa funkcijom gubitka (loss function) pri treniranju modela mašinskog učenja. Ona meri grešku modela na podacima, a ne kvalitet alternative u odluci.
- Funkcija cilja ocenjuje alternative, a [[Funkcija korisnosti|funkcija korisnosti]] ishode.
