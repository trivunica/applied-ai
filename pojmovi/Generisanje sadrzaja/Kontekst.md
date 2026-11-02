---
tip: pojam
aliases: [Context]
izvor: "Zhao, W. X. i dr. (2023). A Survey of Large Language Models. arXiv:2303.18223. https://arxiv.org/abs/2303.18223"
---
# Kontekst (Context)

## Definicija
Tekst i druge informacije koje [[Jezički model|jezički model]] uzima u obzir pri generisanju odgovora: instrukcija ([[Prompt]]), prethodni delovi razgovora i priloženi dokumenti. Ograničen je veličinom kontekstnog prozora.

## Primer
U dugom razgovoru model odgovara u skladu sa prethodnim porukama sve dok one staju u kontekstni prozor.

## Napomene
Kada je kontekst predug, važne informacije mogu biti zanemarene ili pomešane. To se naziva gubitak konteksta i jedan je od izvora grešaka, uz [[Halucinacija|halucinacije]]. U klasičnim n-gram jezičkim modelima kontekst je fiksan broj n prethodnih reči (Zhao i sar., 2023).
