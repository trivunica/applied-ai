---
tip: pojam
aliases: [Decision Threshold, Threshold]
izvor: Fawcett, "An introduction to ROC analysis", Pattern Recognition Letters, 2006
---

# Prag odlučivanja (Decision Threshold)

## Definicija

Prag odlučivanja je [[Rešenje]] koje predstavlja granicu ocene detekcije iznad koje sistem prijavljuje detekciju.

## Primer

Sistem za vizuelnu kontrolu u fabrici Orion svakom delu dodeljuje ocenu koja izražava koliko je verovatno da sadrži defekt. Sistem za vizuelnu kontrolu u fabrici Orion svakom delu dodeljuje ocenu detekcije na osnovu karakteristika snimka. Ako je prag odlučivanja 0,7, sistem prijavljuje delove čija ocena prelazi tu vrednost. Snižavanje praga povećava broj prijavljenih defekata, uključujući i neke ispravne delove, dok podizanje praga može smanjiti broj lažnih uzbuna, ali i povećati broj propuštenih defekata.