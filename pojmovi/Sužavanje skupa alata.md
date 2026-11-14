---
tip: pojam
aliases: [tool scoping, sužavanje skupa alata po koraku]
izvor: "Gan, T., Sun, Q. RAG-MCP: Mitigating Prompt Bloat in LLM Tool Selection via Retrieval-Augmented Generation. arXiv:2505.03275, 2025. https://arxiv.org/abs/2505.03275"
---
# Sužavanje skupa alata (tool scoping)

## Definicija
Sužavanje skupa alata je postupak kojim [[Okruženje agenta|okruženje agenta]] u svakom koraku zadatka nudi [[Jezički model|jezičkom modelu]] samo [[Alat|alate]] potrebne za taj korak.

## Primer
Zadatak servisiranja CNC-07 u pogonu Orion ima četiri koraka: dijagnoza, provera zaliha, nabavka i zakazivanje servisa. U koraku provere zaliha okruženje agenta modelu nudi samo zalihe, rezervacije i rok_isporuke. Ostalih 37 alata i dalje postoji, ali ih model u tom koraku ne vidi, pa ne može greškom da pozove ni nabavka_porudzbina.

## Napomene
Razlikuju se tri pristupa. Statičko sužavanje unapred zadaje skup alata za svaki korak; kod OpenAI-ja mu odgovara opcija allowed_tools. Dinamičko sužavanje pre svakog odgovora pretražuje skup svih alata i izdvaja najrelevantnije; kod OpenAI-ja mu odgovara tool search. Kombinovano sužavanje koristi korake kao granice, a pretragu za izbor unutar njih.

Rizik je da korak dobije preuzak skup ili da pretraga izostavi potreban alat. Zaštita je mali skup osnovnih alata koji je uvek ponuđen i mogućnost da model zatraži širi skup. Problem koji sužavanje rešava opisan je u pojmu [[Preopterećen skup alata]].
