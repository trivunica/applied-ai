---
tip: pojam
aliases: [Testing]
izvor: "Chen, M. i dr. (2021). Evaluating Large Language Models Trained on Code. arXiv:2107.03374. https://arxiv.org/abs/2107.03374"
---
# Testiranje (Testing)

## Definicija
Provera ponašanja koda na unapred definisanim ulazima i očekivanim izlazima, radi otkrivanja grešaka.

## Primer
Za generisanu funkciju piše se skup testova koji proverava rezultate za uobičajene i granične ulaze.

## Napomene
Prolazak testova ne dokazuje da kod nema grešaka, već samo da radi na proverenim slučajevima. Testiranje je jedan od oblika [[Verifikacija|verifikacije]]. Chen i sar. (2021) za ocenu generisanog koda koriste jedinične testove i metriku pass@k, pri čemu je zadatak rešen ako bar jedan od k uzoraka prođe sve testove.
