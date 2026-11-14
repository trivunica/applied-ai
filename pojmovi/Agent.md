---
tip: pojam
aliases: [AI agent, LLM agent, agent zasnovan na jezičkom modelu]
izvor: "Schluntz, E., Zhang, B. Building effective agents. Anthropic, 2024. https://www.anthropic.com/engineering/building-effective-agents"
---
# Agent (agent)

## Definicija
Agent je sistem sastavljen od [[Jezički model|jezičkog modela]] i [[Okruženje agenta|okruženja agenta]], u kome model u petlji bira [[Alat|alate]] i zahteva njihove [[Poziv alata|pozive]] dok ne ostvari zadatak, pri čemu izbor i redosled poziva određuje model tokom rada.

## Primer
Asistent za održavanje u pogonu Orion dobija zadatak da reši pojačane vibracije na CNC-07. Model najpre traži očitavanje vibracija i stanje zaliha, iz rezultata zaključuje da je kvar na vretenu, a zatim traži rezervaciju vretena i zakazivanje servisa. Nijedan od tih koraka nije unapred programiran: svaki sledeći poziv model bira na osnovu rezultata prethodnih.

## Napomene
Agent se razlikuje od toka rada (workflow), u kome program unapred određuje redosled poziva modela i alata. Sistem sa istim modelom i istim alatima, ali sa unapred zadatim redosledom, nije agent.
