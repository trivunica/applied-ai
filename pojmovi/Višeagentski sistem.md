---
tip: pojam
aliases: [multi-agent system, MAS, multiagentski sistem]
izvor: "Wooldridge, M. (2009). An Introduction to MultiAgent Systems, 2. izd. Wiley, pogl. 1; Guo, T. i dr. (2024). Large Language Model Based Multi-agents: A Survey of Progress and Challenges. IJCAI-24, 8048-8057. https://doi.org/10.24963/ijcai.2024/890"
---
# Višeagentski sistem (multi-agent system)

## Definicija
Višeagentski sistem je [[AI tehnologija]] sastavljena od više [[AI agent|AI agenata]] sa podeljenim zadacima, koji razmenjuju rezultate radi zajedničkog cilja.

## Primer
U trećoj, sadašnjoj fazi sistem za dijagnostiku kvarova u fabrici [[Orion Precizni Delovi]] je višeagentski sistem. Zahtev rukovodioca održavanja prima koordinacioni agent, koji zadatke raspoređuje na tri agenta. Agent za senzorske podatke analizira vibracije i temperaturu vretena CNC-07, agent za tehničku dokumentaciju traži dozvoljene vrednosti i proceduru zamene vretena, a agent za troškove procenjuje trošak zamene, uključujući ugovornu kaznu od 400 EUR za dva dana kašnjenja naloga N-2417. Tri agenta rade istovremeno, a koordinacioni agent od njihovih rezultata sastavlja nacrt servisnog naloga.

## Napomene
- Jedan agent koji poziva više alata nije višeagentski sistem. Agent u višeagentskom sistemu sam bira svoje korake, a alat samo izvršava poziv.
- Koordinacioni agent se zove i orkestrator (orchestrator), a ostali agenti izvršioci (workers).
- Podela posla povećava broj poziva modela, pa time i potrošnju tokena i broj koraka koje treba pratiti (vidi [[Praćenje potrošnje tokena]] i [[Distribuirano praćenje]]).
