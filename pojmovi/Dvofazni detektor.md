---
tip: pojam
aliases: [Two-stage Detector]
izvor: Ren, He, Girshick, Sun, "Faster R-CNN: Towards Real-Time Object Detection with Region Proposal Networks", NeurIPS, 2015
---
# Dvofazni detektor (Two-stage Detector)

## Definicija
Detektor u [[Detekcija objekata|detekciji objekata]] koji u prvoj fazi predlaže regione u kojima bi mogao biti [[Objekat|objekat]], a u drugoj svaki predloženi region klasifikuje i doteruje mu [[Granični okvir|granični okvir]].

## Primer
Na snimku hodnika prva faza predloži 300 regiona. Druga faza odbaci one bez osobe, a preostalima dodeli klasu i precizniji okvir.
