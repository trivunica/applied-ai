---
tip: pojam
aliases: [agent loop, agentic loop]
izvor: "Schluntz, E., Zhang, B. (2024). Building effective agents. Anthropic. https://www.anthropic.com/engineering/building-effective-agents; Yao, S. i dr. (2023). ReAct: Synergizing Reasoning and Acting in Language Models. ICLR 2023. arXiv:2210.03629"
---
# Agentska petlja (agent loop)

## Definicija
Agentska petlja je [[Karakteristika|karakteristika]] [[AI agent|AI agenta]] da radi u ponovljenim ciklusima: izabere akciju, izvrši je i njen rezultat uzme kao [[Ulaz|ulaz]] za izbor sledeće akcije. Broj ciklusa nije unapred poznat. Petlja se završava kada agent proceni da je cilj ostvaren ili kada je prekine uslov zaustavljanja zadat spolja, na primer najveći dozvoljeni broj ciklusa ili tokena.

## Primer
Koordinacioni agent sistema za dijagnostiku kvarova u fabrici [[Orion Precizni Delovi]] zadaje agentu za senzorske podatke da utvrdi kako se menjaju vibracije vretena CNC-07. U prvom ciklusu agent traži očitavanja vibracija za poslednjih sedam dana i vidi da rastu. U drugom traži ista očitavanja razvrstana po broju obrtaja i vidi da rastu samo pri visokom broju obrtaja. U trećem traži temperaturu, koja je u granicama. Posle trećeg ciklusa procenjuje da ima dovoljno podataka i vraća zaključak da obrazac odgovara istrošenom ležaju. Za isti zadatak na mašini CNC-09 bilo je potrebno sedam ciklusa, jer su nedostajala očitavanja jednog senzora. Ako agent ne proceni da je završio, sistem prekida analizu kada ona potroši 300.000 tokena, koliko jedna analiza sme da potroši.

## Napomene
- AI agent je tehnologija, a agentska petlja način na koji ona radi. Iz petlje proizlazi [[Mogućnost|mogućnost]] da agent prilagodi korake rezultatima, ali i to da se trajanje i trošak jedne analize ne znaju unapred (vidi [[Praćenje potrošnje tokena]]).
- Ako agent ponavlja akcije koje ne donose nove rezultate i nikada ne proceni da je cilj ostvaren, petlja se ne završava sama, nego tek kada je prekine uslov zaustavljanja ili čovek: to je [[Petlja bez napretka|petlja bez napretka]]. Petlja koju prekine uslov zaustavljanja obično se završava bez rezultata.
- Ponavljanje koje zadaje program, na primer najviše tri pokušaja istog koraka u [[Agentski tok rada|agentskom toku rada]], nije agentska petlja, jer u njemu model ne bira sledeću akciju.
