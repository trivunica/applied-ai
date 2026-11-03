---
tip: pojam
aliases: [Reconstruction Error]
izvor: Sakurada, Yairi, "Anomaly Detection Using Autoencoders with Nonlinear Dimensionality Reduction", MLSDA Workshop, 2014
---
# Greška rekonstrukcije (Reconstruction Error)

## Definicija
Mera razlike između ulaza i njegove rekonstrukcije koju daje [[Autoenkoder|autoenkoder]], npr. srednja kvadratna greška.

## Primer
Autoenkoder naučen na redovnom radu rekonstruiše uobičajen zapis sa greškom 0,02, a zapis noćnog masovnog preuzimanja sa greškom 0,85. Velika greška znači da je ulaz drugačiji od onoga što je mreža naučila.

## Napomene
Koristi se kao ocena anomalije jer autoenkoder dobro rekonstruiše samo ono što liči na podatke na kojima je učio.
