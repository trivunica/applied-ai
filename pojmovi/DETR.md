---
tip: pojam
aliases: [DETR, DEtection TRansformer]
izvor: Carion et al., "End-to-End Object Detection with Transformers", ECCV, 2020
---
# DETR (DEtection TRansformer)

## Definicija
Detektor zasnovan na arhitekturi transformer koji [[Detekcija objekata|detekciju objekata]] posmatra kao direktno predviđanje skupa objekata, bez ručno projektovanih predloga regiona i bez [[Potiskivanje nemaksimalnih predikcija|potiskivanja nemaksimalnih predikcija]].

## Primer
Za snimak hodnika model vraća fiksan broj predikcija, a svaka ili odgovara jednoj osobi ili nosi oznaku "nema objekta". Dve osobe daju dve predikcije bez duplikata.
