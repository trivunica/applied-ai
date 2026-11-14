---
tip: pojam
aliases: [Distribution Shift, Dataset Shift, drift]
izvor: Quiñonero-Candela et al. (ur.), Dataset Shift in Machine Learning, MIT Press, 2009
---

# Promena raspodele podataka (Distribution Shift)

## Definicija

Promena raspodele podataka je vrsta [[Problem|problema]] u kojoj se raspodela podataka na kojima je model obučen razlikuje od raspodele podataka na kojima se primenjuje.

## Primer

Sistem za prediktivno održavanje u fabrici [[Orion Precizni Delovi]] obučen je na očitavanjima vibracija vretena CNC-07 tokom uobičajenog rada. Nakon promene režima obrade, vibracije se sistematski razlikuju od ranijih očitavanja, zbog čega model češće prijavljuje upozorenja i kada nema naznaka predstojećeg otkaza.