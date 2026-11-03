---
tip: pojam
aliases: [Out-of-Distribution Detection, OOD Detection]
izvor: Hendrycks, Gimpel, "A Baseline for Detecting Misclassified and Out-of-Distribution Examples in Neural Networks", ICLR, 2017
---
# Detekcija podataka van distribucije (Out-of-Distribution Detection, OOD Detection)

## Definicija
[[Detekcija|Detekcija]] ulaza koji potiču iz raspodele različite od one na kojoj je model učen.

## Primer
Model za klasifikaciju zvukova u čekaonici naučen je na zvucima čekaonice. Kada dobije snimak sa gradilišta pored klinike, sistem prepoznaje da ulaz ne liči na podatke za učenje, umesto da ga na silu svrsta u neku od poznatih klasa.

## Napomene
Razlikuje se od [[Promena distribucije podataka|promene distribucije podataka]], koja opisuje pojavu, dok se ovde radi o prepoznavanju pojedinačnog ulaza koji je van naučene raspodele.
