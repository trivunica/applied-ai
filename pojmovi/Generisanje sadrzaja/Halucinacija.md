---
tip: pojam
aliases: [Hallucination]
izvor: "Ji, Z. i dr. (2023). Survey of Hallucination in Natural Language Generation. ACM Computing Surveys, 55(12), čl. 248. https://doi.org/10.1145/3571730"
---

# Halucinacija (Hallucination)

## Definicija

Halucinacija je greška generativne AI tehnologije u kojoj model generiše sadržaj koji je uverljiv, ali netačan, nepotkrepljen ili izmišljen, predstavljajući ga kao činjenicu.

## Primer

[[Jezički model]] navodi naučni rad sa autorom, naslovom i godinom objavljivanja koji ne postoje.

## Napomene

Ji i saradnici razlikuju dve vrste halucinacija:

- **Unutrašnja halucinacija (Intrinsic Hallucination):** Generisani sadržaj protivreči informacijama iz izvornog teksta ili konteksta.
- **Spoljašnja halucinacija (Extrinsic Hallucination):** Generisani sadržaj ne može se potvrditi na osnovu izvornog teksta ili konteksta.

- Nedostaci

- **Sklonost generisanju netačnih informacija:** Modeli su optimizovani da generišu verovatne izlaze na osnovu naučenih obrazaca, što ne garantuje činjeničnu tačnost. Zbog toga mogu generisati uverljive, ali netačne informacije.

- Ublažavanje

Rizik od halucinacija može se smanjiti preciznim [[Prompt|promptom]], navođenjem pouzdanih izvora, verifikacijom činjenica i [[Ljudski nadzor|ljudskim nadzorom]].