---
tip: pojam
aliases: [alert threshold, decision threshold]
izvor: "Google, Machine Learning Glossary, pojam classification threshold, developers.google.com/machine-learning/glossary"
---
# Prag upozorenja (alert threshold)

## Definicija
Unapred zadata vrednost [[Predikcija|predikcije]] pri čijem prekoračenju sistem pokreće upozorenje ili predlaže akciju.

## Primer
U fabrici [[Orion Precizni Delovi]] sistem za prediktivno održavanje ima prag od 25% procenjene verovatnoće otkaza vretena u narednih deset dana. Za mašinu CNC-07 procena je 30%, prag je prekoračen, pa sistem predlaže zamenu vretena pre planiranog servisa. Za mašinu čija je procena 10% sistem ne reaguje.

## Napomene
- Postavljanje praga je [[Odluka|odluka]], a ne tehnički detalj. Niži prag daje više nepotrebnih zamena, viši više propuštenih otkaza.
- Prag se može obrazložiti poređenjem ishoda. U primeru [[Funkcija korisnosti|funkcije korisnosti]] zamena vretena postaje bolja od nastavka rada kada verovatnoća otkaza pređe oko 29% (25 / 85), pa je prag od 25% blago konzervativan.
- Isti prag drugačije radi kada je procena neprecizna, jer tada i ista vrednost praga daje više grešaka.
