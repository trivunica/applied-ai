---
tip: pojam
aliases: [Non-Maximum Suppression, NMS]
izvor: Neubeck, Van Gool, "Efficient Non-Maximum Suppression", ICPR, 2006
---
# Potiskivanje nemaksimalnih predikcija (Non-Maximum Suppression, NMS)

## Definicija
Postupak koji od više preklapajućih [[Granični okvir|graničnih okvira]] za isti [[Objekat|objekat]] zadržava onaj sa najvišom ocenom pouzdanosti, a one čiji [[Preklapanje preko unije|IoU]] sa njim prelazi zadati prag odbacuje.

## Primer
Za jednu osobu u hodniku model predvidi pet okvira sa ocenama 0,95, 0,90, 0,85, 0,80 i 0,70. Zadržava se okvir sa ocenom 0,95, a ostali se odbacuju jer im IoU sa njim prelazi 0,5.
