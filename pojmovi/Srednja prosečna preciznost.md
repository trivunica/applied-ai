---
tip: pojam
aliases: [Mean Average Precision, mAP]
izvor: Lin et al., "Microsoft COCO: Common Objects in Context", ECCV, 2014
---
# Srednja prosečna preciznost (Mean Average Precision, mAP)

## Definicija
Aritmetička sredina [[Prosečna preciznost|prosečne preciznosti]] po svim klasama detektora.

## Primer
Detektor ima AP 0,90 za klasu "osoba", 0,80 za "bolnička kolica" i 0,70 za "torba". mAP je (0,90 + 0,80 + 0,70) / 3 = 0,80.

## Napomene
Tačna definicija zavisi od skupa za testiranje. U skupu Pascal VOC računa se pri IoU od 0,5, a u skupu COCO prosek je i po više pragova IoU, od 0,5 do 0,95. Pri poređenju rezultata mora se navesti koja se koristi.
