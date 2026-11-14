---
tip: pojam
aliases: [Decision Threshold, Threshold]
izvor: Fawcett, "An introduction to ROC analysis", Pattern Recognition Letters, 2006
---

# Prag odlučivanja (Decision Threshold)

## Definicija

Prag odlučivanja je [[Rešenje]] koje predstavlja granicu ocene detekcije iznad koje sistem prijavljuje detekciju.

## Primer

Sistem za vizuelnu kontrolu u fabrici [[Orion Precizni Delovi]] svakom delu dodeljuje ocenu detekcije koja izražava koliko je verovatno da deo sadrži defekt. Ako je prag odlučivanja 0,7, sistem prijavljuje delove čija ocena prelazi tu vrednost. Snižavanje praga povećava broj prijavljenih defekata, uključujući i neke ispravne delove, dok podizanje praga može smanjiti broj lažnih upozorenja, ali i povećati broj propuštenih defekata.

## Napomene

Pomeranje praga razmenjuje [[Lažno pozitivna detekcija|lažno pozitivne]] i [[Lažno negativna detekcija|lažno negativne]] detekcije. Prag odlučivanja se odnosi na ocenu detekcije ([[Analiza sadržaja]]). Granica verovatnoće predikcije kod [[Odlučivanje|odlučivanja]] je poseban pojam (Prag upozorenja) i nije obrađena u ovoj osnovi.
