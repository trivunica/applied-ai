---
tip: pojam
aliases: [retrieval-augmented generation, RAG]
izvor: "Lewis, P. i dr. (2020). Retrieval-Augmented Generation for Knowledge-Intensive NLP Tasks. Advances in Neural Information Processing Systems 33 (NeurIPS 2020)"
---
# Dopuna generisanja pretraživanjem (retrieval-augmented generation, RAG)

## Definicija
Dopuna generisanja pretraživanjem je [[Rešenje|rešenje]] za [[Generisanje sadržaja|generisanje sadržaja]] u kome se pre generisanja iz zadatog skupa dokumenata pronađu delovi relevantni za upit i dodaju u [[Kontekst modela|kontekst modela]], tako da model izlaz zasniva na njima, a ne samo na onome što je naučio.

## Primer
Tehnolog u fabrici [[Orion Precizni Delovi]] traži nacrt radne instrukcije za obradu kućišta na mašini CNC-07. Pre generisanja sistem u tehničkoj dokumentaciji pronađe uputstvo za CNC-07, tabelu dozvoljenih brzina za taj čelik i postojeću instrukciju za slično kućište, pa ih doda u kontekst. Model brzinu obrade uzima iz tabele umesto da je izmisli, a nacrt navodi iz kog dokumenta je preuzeta.

## Napomene
- Smanjuje [[Halucinacija|halucinacije]], ali ih ne uklanja. Model i dalje može pogrešno da pročita pronađeni deo, a pretraga može da pronađe pogrešan dokument.
- Svaki dokument u skupu postaje mogući put za [[Ubacivanje instrukcija|ubacivanje instrukcija]].
- Kako pretraga radi iznutra (embedding, vektorska baza) je crna kutija i ne opisuje se.
- Za razliku od [[Ponovno treniranje|ponovnog treniranja]], model se ne menja. Kada se dokumentacija promeni, dovoljno je ažurirati skup dokumenata.
