---
tip: pojam
aliases: [Tokenization]
izvor: "Sennrich, R., Haddow, B., Birch, A. (2016). Neural Machine Translation of Rare Words with Subword Units. ACL 2016, str. 1715–1725. https://doi.org/10.18653/v1/P16-1162"
---
# Tokenizacija (Tokenization)

## Definicija
Deljenje teksta na manje jedinice – tokene (reči, delove reči ili znakove) – koje [[Jezički model|jezički model]] obrađuje. Svaki token se zatim pretvara u numeričku reprezentaciju ([[Embedding]]).

## Primer
Reč „generisanje“ može biti podeljena na tokene „generis“ i „anje“.

## Napomene
Token nije isto što i reč. Dužina [[Kontekst|konteksta]] i ograničenja modela mere se u tokenima, a ne u rečima. Česta tehnika je kodiranje parova bajtova (BPE), kojim se retke reči razlažu na češće podreči (Sennrich i sar., 2016).
