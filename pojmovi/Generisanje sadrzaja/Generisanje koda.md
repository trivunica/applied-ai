---
tip: pojam
aliases: [Code generation]
izvor: "Chen, M. i dr. (2021). Evaluating Large Language Models Trained on Code. arXiv:2107.03374. https://arxiv.org/abs/2107.03374"
---
# Generisanje koda (Code generation)

## Definicija
Stvaranje programskog koda na osnovu opisa zadatka, konteksta ili postojećeg koda, najčešće pomoću [[LLM|velikog jezičkog modela]].

## Primer
Programer opiše funkciju na srpskom, a model predloži njenu implementaciju i prateće testove.

## Napomene
Generisani kod treba proveriti [[Testiranje|testiranjem]] i pregledom, jer može sadržati greške i [[Ranjivost|ranjivosti]]. Chen i sar. (2021) funkcionalnu ispravnost generisanog koda mere skupom testova (HumanEval) i metrikom pass@k.
