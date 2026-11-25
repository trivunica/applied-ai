---
tip: pojam
aliases: [MCP]
izvor: "Model Context Protocol Specification, revizija 2026-07-28. https://modelcontextprotocol.io/specification/2026-07-28"
---
# Model Context Protocol (MCP)

## Definicija
Model Context Protocol (MCP) je otvoreni protokol po kome aplikacija koja koristi [[Veliki jezički model|veliki jezički model]] na jedinstven način pristupa spoljnim sistemima: od njih pribavlja podatke koji postaju [[Ulaz|ulaz]] modela, a na zahtev modela poziva njihove alate. Spoljni sistem se izlaže preko MCP servera, a aplikacija mu pristupa preko MCP klijenta.

## Primer
Sistem za dijagnostiku kvarova u fabrici [[Orion Precizni Delovi]] pristupa podacima preko tri MCP servera: jedan je ispred ERP sistema, drugi ispred sistema za prikupljanje senzorskih podataka, a treći ispred sistema za tehničku dokumentaciju. Server ispred senzorskog sistema nudi alat koji za zadatu mašinu i period vraća očitavanja vibracija i temperature, a server ispred ERP sistema alat koji vraća stanje zaliha za zadati deo. Server ispred sistema za tehničku dokumentaciju nudi uputstva proizvođača mašina kao resurse, koje aplikacija dodaje u kontekst modela. Kada je sistem iz druge faze, sa jednim AI agentom, prešao u treću, sa tri agenta, serveri nisu menjani: svaki agent je dobio pristup samo serverima koji su mu potrebni, na primer agent za troškove samo serveru ispred ERP sistema.

## Napomene
- MCP server nudi tri vrste sadržaja: resurse, odnosno podatke koje aplikacija dodaje u [[Kontekst modela|kontekst modela]], alate, odnosno funkcije koje poziva model, i promptove, odnosno šablone poruka koje bira korisnik. U kontekst modela ulazi i rezultat svakog poziva alata.
- MCP je nastao da zameni posebnu integraciju za svaki par aplikacije i spoljnog sistema. Nije [[AI tehnologija]], jer sam ne proizvodi izlaz, a nije ni [[Rešenje|rešenje]]: rešenje je dopuna konteksta modela podacima iz pouzdanih izvora, koja smanjuje [[Halucinacija|halucinacije]], a MCP je standardan način da se ta dopuna izvede.
- Protokol sam ne može da nametne bezbednosna pravila. Koje podatke server izlaže i ko sme da ih čita određuju server i aplikacija (vidi [[Prekomerno izlaganje resursa]]). Poziv alata može i da ostane bez odgovora (vidi [[Istek vremena alata]]).
