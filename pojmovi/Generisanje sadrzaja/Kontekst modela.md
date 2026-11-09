---
tip: pojam
aliases: [Context]
izvor: "Zhao, W. X. i dr. (2023). A Survey of Large Language Models. arXiv:2303.18223. https://arxiv.org/abs/2303.18223"
---
# Kontekst modela (Context)

## Definicija
Kontekst modela predstavlja skup informacija koje [[Jezički model|jezički model]] uzima u obzir prilikom generisanja odgovora. Može obuhvatati instrukcije ([[Prompt]]), prethodne poruke u razgovoru i priložene dokumente. Količina informacija koju model može da obradi u jednom trenutku ograničena je veličinom kontekstnog prozora (context window).

## Primer
Korisnik u razgovoru prvo definiše određeni zadatak, a zatim daje dodatne instrukcije i primere. Model koristi prethodne poruke i nove informacije kako bi generisao odgovor u skladu sa zadatim kontekstom.

## Napomene
Nedostaci - Ograničen kontekstni prozor: Model može da obradi samo određenu količinu informacija u jednom trenutku. Kada ulaz premaši raspoloživi kontekstni prozor, deo prethodnih informacija mora biti izostavljen ili skraćen.

Mogućnosti - Učenje iz konteksta (In-Context Learning): Model može da prepozna zadatak i generiše odgovarajući odgovor na osnovu instrukcija i primera navedenih u promptu, bez dodatnog treniranja ili ažuriranja parametara modela (Zhao i sar., 2023).
