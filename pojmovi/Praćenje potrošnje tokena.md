---
tip: pojam
aliases: [token usage tracking, token tracking]
izvor: "OpenTelemetry Semantic Conventions for Generative AI: atributi gen_ai.usage.input_tokens i gen_ai.usage.output_tokens, metrika gen_ai.client.token.usage. https://github.com/open-telemetry/semantic-conventions-genai"
---
# Praćenje potrošnje tokena (token usage tracking)

## Definicija
Praćenje potrošnje tokena je vrsta [[Evaluacija|evaluacije]] u kojoj se za svaki poziv modela meri broj tokena u ulazu i u izlazu, a zbirovi po koraku, agentu i celom izvršavanju upoređuju se sa [[Ograničenje|ograničenjima]] i [[Metrika uspeha|metrikama uspeha]] slučaja korišćenja koje se odnose na trošak.

## Primer
Platforma za praćenje u fabrici [[Orion Precizni Delovi]] za svaku analizu sabira tokene po agentima i poredi ih sa metrikom uspeha slučaja korišćenja, brojem tokena po analizi. Prosečna analiza troši oko 90.000 tokena, od toga agent za tehničku dokumentaciju oko 60.000. Inženjer za AI sisteme vidi da taj agent na početku u kontekst modela dodaje celo uputstvo proizvođača mašine, oko 20.000 tokena, iako mu treba samo poglavlje o zameni vretena. Pošto se ceo kontekst šalje u svakom pozivu modela, uputstvo se računa u ulazu svakog od tri poziva tog agenta. Kada MCP server ispred sistema za tehničku dokumentaciju počne da vraća samo traženo poglavlje, prosečna analiza pada na oko 40.000 tokena.

## Napomene
- Tokeni se broje posebno za ulaz i za izlaz, jer se obično različito naplaćuju. Ulaz svakog poziva sadrži ceo dotadašnji kontekst modela, pa u [[Agentska petlja|agentskoj petlji]] ukupan broj ulaznih tokena raste brže od broja ciklusa.
- Broj tokena se najčešće čita iz [[Distribuirano praćenje|traga]], gde je zapisan uz svaki korak koji je poziv modela, pa se može sabrati po agentu, analizi ili danu.
- Kada se potrošnja prati tokom izvršavanja, a ne tek posle, praćenje postaje i [[Rešenje|rešenje]]: sistem prekida analizu kada ona pređe 300.000 tokena (vidi [[Beskonačna agentska petlja]]).
