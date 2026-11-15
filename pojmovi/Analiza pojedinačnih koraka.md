---
tip: pojam
aliases: [span-level analysis, failure attribution]
izvor: "Zhang, S. i dr. (2025). Which Agent Causes Task Failures and When? On Automated Failure Attribution of LLM Multi-Agent Systems. ICML 2025. arXiv:2505.00212"
---
# Analiza pojedinačnih koraka (span-level analysis)

## Definicija
Analiza pojedinačnih koraka je vrsta [[Evaluacija|evaluacije]] u kojoj se ulaz i izlaz svakog koraka iz [[Distribuirano praćenje|traga]] ocenjuju zasebno, da bi se pronašao korak u kome je nastala [[Greška|greška]] i agent koji ga je izvršio.

## Primer
Rukovodilac održavanja u fabrici [[Orion Precizni Delovi]] odbija nacrt servisnog naloga koji predlaže zamenu vretena na CNC-07, jer se zaključak ne slaže sa očitavanjima. Inženjer za AI sisteme otvara trag te analize na platformi za praćenje i ocenjuje korake redom. Agent za senzorske podatke vratio je ispravnu vrednost vibracija od 2,8 mm/s, a agent za tehničku dokumentaciju ispravnu granicu proizvođača od 4,5 mm/s. U sledećem koraku, pozivu modela koordinacionog agenta, model je od ta dva ispravna podatka zaključio da su vibracije iznad dozvoljene granice. To je prvi korak koji je od ispravnog ulaza dao neispravan izlaz, pa je greška nastala u njemu, a ne u senzorima, MCP serverima ni ostalim agentima. Da nalog nije odbijen, nepotrebna zamena vretena koštala bi 2.300 EUR.

## Napomene
- Evaluacija celog izvršavanja kaže da li je nalog ispravan, a analiza pojedinačnih koraka kaže gde je greška nastala, pa je njen nalaz osnova za [[Rešenje|rešenje]]: u primeru se poređenje vrednosti sa granicom premešta iz poziva modela u alat koji poredi brojeve. Bez [[Distribuirano praćenje|distribuiranog praćenja]] ova analiza nije moguća, jer nema zapisa koraka.
- Korak u kome je greška nastala obično je prvi korak koji je od ispravnog ulaza dao neispravan izlaz. Strožiji kriterijum je kontrafaktički: to je najraniji korak čija bi ispravka dovela do ispravnog konačnog izlaza, pa se ne računaju greške koje nisu uticale na ishod.
- Korake može da ocenjuje čovek ili [[Veliki jezički model kao evaluator|veliki jezički model kao evaluator]], ali automatsko pronalaženje koraka zasad je nepouzdano: u istraživanju Zhang i dr. (2025) najbolji metod je odgovornog agenta pogodio u 53,5% slučajeva, a odgovorni korak u samo 14,2%.
