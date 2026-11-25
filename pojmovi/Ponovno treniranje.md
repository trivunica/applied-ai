---
tip: pojam
aliases: [retraining]
izvor: "Gama, J. i dr. (2014). A Survey on Concept Drift Adaptation. ACM Computing Surveys, 46(4), čl. 44. https://doi.org/10.1145/2523813"
---
# Ponovno treniranje (retraining)

## Definicija
Ponovno treniranje je [[Rešenje|rešenje]] za [[Promena raspodele podataka|promenu raspodele podataka]] u kome se model trenira na novijim podacima, da bi se [[Metrika uspeha|metrike uspeha]] vratile na prihvatljiv nivo.

## Primer
[[Praćenje modela u radu]] pokazalo je da sistem za prediktivno održavanje u fabrici [[Orion Precizni Delovi]] posle prelaska na novog dobavljača čelika izdaje previše upozorenja. Tim sakupi očitavanja vibracija iz poslednja dva meseca i iz evidencije otkaza i servisa označi koja su se završila otkazom. Model se ponovo trenira na starim i novim podacima. Pre nego što zameni stari, prolazi [[Evaluacija|evaluaciju]] na podacima iz poslednje dve nedelje, koje nije video.

## Napomene
- Treba sačekati da se sakupi dovoljno obeleženih novih podataka. Otkaz se vidi tek kada se desi, pa za to vreme mogu biti potrebni [[Rezervni postupak|rezervni postupak]] ili [[Ljudski nadzor|ljudski nadzor]].
- Ponovo treniran model je nov model i može imati nove greške. Zato se evaluira pre puštanja i čuva se prethodna verzija za vraćanje.
- Automatsko ponovno treniranje na podacima iz rada otvara put [[Trovanje podataka|trovanju podataka]].
