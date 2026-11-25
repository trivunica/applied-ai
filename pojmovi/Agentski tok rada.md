---
tip: pojam
aliases: [agentic workflow, workflow]
izvor: "Schluntz, E., Zhang, B. (2024). Building effective agents. Anthropic. https://www.anthropic.com/engineering/building-effective-agents"
---
# Agentski tok rada (agentic workflow)

## Definicija
Agentski tok rada je [[AI tehnologija]] u kojoj se pozivi [[Veliki jezički model|velikog jezičkog modela]] i alata izvršavaju po putanji koju unapred zadaje program, a ne model.

## Primer
U prvoj fazi sistem za dijagnostiku kvarova u fabrici [[Orion Precizni Delovi]] bio je agentski tok rada sa tri fiksna koraka. Za svaki zahtev program učitava očitavanja vibracija vretena za poslednjih sedam dana, proverava u ERP sistemu stanje rezervnog vretena i od velikog jezičkog modela traži nacrt servisnog naloga na osnovu ta dva rezultata. Model piše nacrt, ali ne bira koje podatke će pribaviti. Zato tok rada ne proverava ni temperaturu ni istoriju servisa, čak ni kada su potrebne za utvrđivanje uzroka kvara.

## Napomene
- Kod [[AI agent|AI agenta]] sledeći korak bira model. Tok rada je predvidljiviji i jeftiniji, ali ne može da uradi korak koji program nije predvideo.
- Model može da bira između grana koje je program predvideo, na primer da zahtev usmeri na jednu od dve unapred napisane putanje, ali ne može da uvede nov korak.
- Pridev agentski ne znači da je u pitanju AI agent: i tokovi rada i agenti zovu se agentski sistemi. U delu literature agentskim tokom rada naziva se svaki višekoračni rad modela, uključujući i AI agenta. Ova baza koristi uži smisao.
