---
tip: pojam
aliases: [AI agent, agent, LLM agent, agent zasnovan na jezičkom modelu]
izvor: "Schluntz, E., Zhang, B. (2024). Building effective agents. Anthropic. https://www.anthropic.com/engineering/building-effective-agents; ISO/IEC 22989:2022, Information technology - Artificial intelligence - Artificial intelligence concepts and terminology, 3.1.1 (AI agent)"
---
# AI agent (AI agent)

## Definicija
AI agent je [[AI tehnologija]] u kojoj [[Veliki jezički model|veliki jezički model]] radi zadatog cilja sam bira niz akcija, najčešće pozive alata, i svaku sledeću akciju bira na osnovu rezultata prethodnih.

## Primer
U drugoj fazi sistem za dijagnostiku kvarova u fabrici [[Orion Precizni Delovi]] bio je jedan AI agent. Rukovodilac održavanja mu zadaje cilj: utvrdi zašto rastu vibracije vretena mašine CNC-07 i pripremi nacrt servisnog naloga. Agent prvo traži očitavanja vibracija i temperature za poslednjih sedam dana. Vibracije rastu, a temperatura je u granicama, pa na osnovu toga bira sledeći korak: iz tehničke dokumentacije traži dozvoljene vibracije za ležaj vretena, a iz evidencije otkaza ranije kvarove vretena istog tipa na CNC-07 i CNC-09. Kada zaključi da je verovatan uzrok istrošen ležaj, proverava u ERP sistemu da li je rezervno vreteno na stanju i piše nacrt naloga. Da je uz vibracije rasla i temperatura, agent bi prvo potražio u evidenciji servisa kada je vreteno poslednji put podmazivano.

## Napomene
- Baza koristi uži smisao pojma: akcije bira veliki jezički model. Po ISO/IEC 22989 (3.1.1) AI agent je svaki automatizovani entitet koji opaža okruženje, reaguje na njega i deluje radi svojih ciljeva, pa bi agent bio i regulator temperature ili program za šah. Takvi sistemi ovde nisu AI agenti.
- Kod [[Agentski tok rada|agentskog toka rada]] putanju koraka unapred zadaje program, a kod AI agenta bira je model. Više AI agenata koji sarađuju čine [[Višeagentski sistem|višeagentski sistem]].
- AI agent obično kombinuje vrste AI tehnologije: tumači očitavanja ([[Analiza sadržaja|analiza sadržaja]]), piše nacrt naloga ([[Generisanje sadržaja|generisanje sadržaja]]) i bira akcije. Nije svaka njegova akcija [[Odluka|odluka]]: čitanje očitavanja ne menja stanje fabrike, a izdavanje servisnog naloga menja, pa nalog postaje važeći tek kada ga odobri rukovodilac održavanja ([[Čovek u petlji|čovek u petlji]]).
- AI agent bira korake, ali ne i cilj, koji mu zadaje čovek. Zato se ovde ne zove autonomnim, iako je izraz autonomni agent čest u literaturi: po ISO/IEC 22989 (3.1.5) autonoman je sistem koji može da promeni i svoj cilj.
