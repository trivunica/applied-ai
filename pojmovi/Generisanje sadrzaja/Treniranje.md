---
tip: pojam
aliases: [Training]
izvor: "Goodfellow, I., Bengio, Y., Courville, A. (2016). Deep Learning. MIT Press. http://www.deeplearningbook.org"
---
# Treniranje (Training)

## Definicija
Postupak podešavanja parametara [[Model|modela]] na osnovu [[Podaci|podataka]], tako da model što bolje reprodukuje [[Raspodela|raspodelu]] podataka ili ispravno rešava zadati zadatak.

## Primer
[[Jezički model]] se trenira tako da što bolje predviđa sledeći token u velikom skupu tekstova.

## Napomene
Treniranje je odvojeno od upotrebe modela. Nakon treniranja, model generiše sadržaj bez ponovnog učenja iz svakog zahteva. Ne treba ga mešati sa [[Evaluacija|evaluacijom]], kojom se proverava naučeno.
