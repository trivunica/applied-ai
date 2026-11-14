---
tip: pojam
aliases: [adversarial example, evasion attack]
izvor: "NIST AI 100-2e2025, Adversarial Machine Learning: A Taxonomy and Terminology of Attacks and Mitigations, odeljak o napadima izbegavanja (evasion), https://doi.org/10.6028/NIST.AI.100-2e2025"
---
# Adversarijalni primer (adversarial example)

## Definicija
Adversarijalni primer je [[Problem|problem]] u kome napadač namerno izmeni [[Ulaz|ulaz]] AI tehnologije, često tako malo da čovek promenu ne primećuje, da bi tehnologija nad tim ulazom proizvela izlaz koji napadač želi.

## Primer
Sistem za vizuelnu kontrolu u fabrici [[Orion Precizni Delovi]] otkriva pukotine na kućištima ležajeva. Neko ko zna kako sistem radi nanese tanku traku specijalne boje preko pukotine. Kontroloru kvaliteta deo i dalje izgleda napuklo, ali sistem ga ocenjuje kao ispravan. Defektan deo prolazi kontrolu, što je [[Lažno negativna detekcija|lažno negativna detekcija]].

## Napomene
- Napad u kome se koristi adversarijalni primer zove se napad izbegavanja (evasion attack). Dešava se dok je sistem u upotrebi, za razliku od [[Trovanje podataka|trovanja podataka]], koje se dešava pri treniranju.
- [[Promena raspodele podataka]] takođe menja ulaz, ali bez namere. Adversarijalni primer pretpostavlja napadača.
- U fabrici je ovaj problem manje verovatan nego u sajber bezbednosti, ali pokazuje zašto [[Robusnost|robusnost]] na prirodne promene ne garantuje robusnost na napad.
