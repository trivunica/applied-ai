---
tip: pojam
aliases: [Intersection over Union, IoU, Jaccard index]
izvor: Everingham et al., "The Pascal Visual Object Classes (VOC) Challenge", International Journal of Computer Vision, 2010
---
# Preklapanje preko unije (Intersection over Union, IoU)

## Definicija
Mera preklapanja dva [[Granični okvir|granična okvira]], jednaka odnosu površine njihovog preseka i površine njihove unije, sa vrednostima od 0 do 1.

## Primer
Okvir koji je predvideo sistem ima površinu 100, ručno nacrtani okvir takođe 100, a preklapaju se na površini 60. Unija je 100 + 100 - 60 = 140, pa je IoU 60 / 140, što je približno 0,43.

## Napomene
Detekcija se obično smatra tačnom kada je IoU sa ručno označenim okvirom najmanje 0,5, ali je to konvencija pojedinih skupova za testiranje, a ne deo definicije.
