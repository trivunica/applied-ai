---
tip: pojam
aliases: [ROC Curve, ROC-AUC, AUC, Receiver Operating Characteristic]
izvor: Fawcett, "An introduction to ROC analysis", Pattern Recognition Letters, 2006
---
# ROC kriva i površina ispod krive (ROC Curve, ROC-AUC)

## Definicija
ROC kriva prikazuje odnos stope tačno pozitivnih (odziv) i stope [[Lažno pozitivna detekcija|lažno pozitivnih]] detekcija za sve vrednosti [[Prag odlučivanja|praga odlučivanja]]. Površina ispod nje (AUC) jednaka je verovatnoći da sistem nasumično izabran pozitivan primerak oceni višom ocenom od nasumično izabranog negativnog.

## Primer
Detektor zloupotreba iz prethodnih primera pri jednom pragu ima stopu tačno pozitivnih 0,75 i stopu lažno pozitivnih približno 0,015. Pri nižem pragu stope su redom 0,95 i približno 0,08. Svaki prag daje jednu tačku ROC krive.

## Napomene
AUC od 0,5 odgovara nasumičnom pogađanju, a 1 savršenom razlikovanju. Pri jakoj [[Neuravnoteženost klasa|neuravnoteženosti klasa]] može delovati optimističnije nego [[Kriva preciznosti i odziva|kriva preciznosti i odziva]].
