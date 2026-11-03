---
tip: pojam
aliases: [R-CNN, Region-based Convolutional Neural Network]
izvor: Girshick, Donahue, Darrell, Malik, "Rich Feature Hierarchies for Accurate Object Detection and Semantic Segmentation", CVPR, 2014
---
# R-CNN (Region-based Convolutional Neural Network)

## Definicija
[[Dvofazni detektor|Dvofazni detektor]] koji kandidate regiona dobija spoljašnjim algoritmom (selektivnom pretragom), a svaki region zasebno obrađuje konvolucionom neuronskom mrežom radi klasifikacije.

## Primer
Za jedan snimak iz hodnika izdvaja se oko 2000 regiona i svaki se posebno propušta kroz mrežu. Zato je obrada jednog snimka spora i neupotrebljiva za nadzor u realnom vremenu.
