---
tip: pojam
aliases: [Faster R-CNN, Faster Region-based Convolutional Neural Network]
izvor: Ren, He, Girshick, Sun, "Faster R-CNN: Towards Real-Time Object Detection with Region Proposal Networks", NeurIPS, 2015
---
# Faster R-CNN (Faster Region-based Convolutional Neural Network)

## Definicija
Unapređenje [[R-CNN|R-CNN]] detektora u kome kandidate regiona predlaže posebna mreža za predlog regiona (RPN) koja deli konvolucione slojeve sa mrežom za klasifikaciju, pa se slika obrađuje jednom.

## Primer
Isti snimak hodnika obrađuje se jednim prolazom kroz zajedničke slojeve, a mreža za predlog regiona odmah predlaže oblasti ispred vrata serverske sobe i pored kolica.
