---
tip: pojam
aliases: [distributed tracing, tracing, LLM tracing]
izvor: "OpenTelemetry, Glossary (Distributed tracing, Trace, Span). https://opentelemetry.io/docs/concepts/glossary/; Sigelman, B. H. i dr. (2010). Dapper, a Large-Scale Distributed Systems Tracing Infrastructure. Google Technical Report dapper-2010-1"
---
# Distribuirano praćenje (distributed tracing)

## Definicija
Distribuirano praćenje je [[Rešenje|rešenje]] u kome se izvršavanje jednog zahteva upućenog [[AI tehnologija|AI tehnologiji]] beleži kao trag (trace), odnosno stablo koraka (span). Korak je jedna operacija, na primer poziv modela, poziv alata ili rad jednog agenta, zabeležena sa vremenom početka i kraja, ulazom, izlazom i vezom ka koraku koji ju je pokrenuo. Korake beleže svi sistemi kroz koje zahtev prolazi, pa se iz traga vidi u kom koraku i u kom sistemu je nastao [[Problem|problem]].

## Primer
Sistem za dijagnostiku kvarova u fabrici [[Orion Precizni Delovi]] šalje korake na platformu za praćenje (Arize Phoenix). Koren traga jedne analize je zahtev koordinacionom agentu, ispod njega su koraci tri agenta, a ispod svakog agenta njegovi pozivi modela i alata. Korake ispod poziva alata beleže MCP serveri, na primer upit koji MCP server ispred ERP sistema šalje ERP-u. Svi koraci jedne analize nose isti identifikator traga, iako ih beleže različiti sistemi. Jedna analiza kvara na CNC-09 prekinuta je kada je potrošila 300.000 tokena. Inženjer za AI sisteme u njenom tragu vidi da je agent za troškove dvanaest puta pozvao alat za stanje zaliha i da se svaki poziv završio istekom vremena, a iz koraka koje je zabeležio MCP server vidi da ERP sistem tada nije odgovarao. Bez traga bi se znalo samo da je analiza prekinuta.

## Napomene
- Distribuirano znači da trag prolazi kroz više sistema: aplikaciju sa agentima, MCP servere i sisteme iza njih. Kada se sve izvršava u jednom procesu, isti postupak se zove samo praćenje (tracing).
- Praćenje ne smanjuje verovatnoću problema, nego njegovu posledicu: uzrok se brže pronalazi i otklanja. Uz to daje podatke za [[Evaluacija|evaluaciju]]: [[Veliki jezički model kao evaluator|veliki jezički model kao evaluator]] ocenjuje izlaze zabeležene u tragu, [[Praćenje potrošnje tokena|praćenje potrošnje tokena]] sabira tokene po koracima, a [[Analiza pojedinačnih koraka|analiza pojedinačnih koraka]] traži korak u kome je nastala greška.
- Trag čuva ulaze i izlaze modela i alata, pa i sve podatke koje je agent pročitao. Ako agent pročita podatke koje ne sme da vidi, oni ostaju i u tragu, dostupni svima koji imaju pristup platformi za praćenje. Tako ovo rešenje može da uvede nov problem, [[Prekomerno izlaganje resursa|prekomerno izlaganje resursa]].
