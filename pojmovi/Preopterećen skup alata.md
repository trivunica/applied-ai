---
tip: pojam
aliases: [tool overload, prompt bloat]
izvor: "Gan, T., Sun, Q. RAG-MCP: Mitigating Prompt Bloat in LLM Tool Selection via Retrieval-Augmented Generation. arXiv:2505.03275, 2025. https://arxiv.org/abs/2505.03275"
---
# Preopterećen skup alata (tool overload)

## Definicija
Preopterećen skup alata je skup [[Alat|alata]] ponuđen [[Jezički model|jezičkom modelu]] za jedan odgovor, toliko velik ili sa toliko sličnih alata da model merljivo češće bira pogrešan alat nego iz manjeg skupa koji sadrži isti potreban alat.

## Primer
Asistent u pogonu Orion za svaki odgovor dobija svih 40 alata, među kojima su zakazi_servis, zakazi_odrzavanje i zakazi_termin_odrzavanja. Kada treba da zakaže popravku vretena na CNC-07, model bira zakazi_termin_odrzavanja, koji upisuje redovan pregled. Kada mu se ponude samo tri alata potrebna za zakazivanje popravke, bira zakazi_servis. U zapisima rada ista zamena se ponavlja kod različitih mašina, pa je problem u skupu alata, a ne u pojedinačnoj odluci.

## Napomene
U radu RAG-MCP tačnost izbora alata je 13,62% kada model vidi sve opise alata, a 43,13% kada mu se prethodno izdvoje samo relevantni alati (preprint; vrednosti zavise od modela i testa). Vodič OpenAI-ja za pozivanje funkcija okvirno preporučuje manje od 20 funkcija na početku poteza, jer se definicije računaju u kontekst i naplaćuju kao ulazni tokeni.

Pojam se odnosi na skup ponuđen za jedan odgovor, a ne na ukupan broj alata u sistemu. Rešenje je opisano u pojmu [[Sužavanje skupa alata]].
