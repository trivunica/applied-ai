---
tip: pojam
aliases: [MCP resource exposure, excessive data exposure, over-sharing]
izvor: "OWASP API Security Top 10 (2019), API3:2019 Excessive Data Exposure. https://api-security.owasp.org/editions/2019/en/0xa3-excessive-data-exposure; Model Context Protocol Specification, revizija 2026-07-28, Resources (Security Considerations)"
---
# Prekomerno izlaganje resursa (MCP resource exposure)

## Definicija
Prekomerno izlaganje resursa je [[Problem|problem]] u kome izvor podataka, najčešće [[Model Context Protocol|MCP]] server, [[AI agent|AI agentu]] daje više podataka nego što mu je potrebno za zadatak, pa podaci koje agent ne treba da vidi ulaze u [[Kontekst modela|kontekst modela]] i odatle mogu da dospeju u izlaz agenta, njegove akcije ili trag izvršavanja.

## Primer
Agent za troškove u fabrici [[Orion Precizni Delovi]] procenjuje trošak zamene vretena na CNC-07 i preko MCP servera ispred ERP sistema poziva alat koji vraća troškove proizvodnje po mašini. Server je napravljen tako da vraća ceo zapis iz ERP sistema, pa uz troškove mašine vraća i troškove rada po operateru, sa imenima i zaradama. Agent te podatke nije tražio, ali oni ulaze u kontekst modela. U nacrt servisnog naloga, koji čitaju i operateri, agent upisuje da prekovremeni sat jedinog sertifikovanog operatera u drugoj smeni košta 8 EUR, pa njegova zarada postaje poznata svima koji čitaju nalog. Zarade svih operatera na CNC-07 ostaju i u tragu analize na platformi za praćenje. Agent nije uradio ništa što mu nije dozvoljeno, a ipak je prekršeno ograničenje slučaja korišćenja da sistem čita samo podatke potrebne za dijagnostiku.

## Napomene
- Problem nastaje na izvoru podataka, ali ga omogućava način rada AI agenta: agent sam bira šta će da pročita, a sve što pročita ulazi u kontekst modela, iz koga model ne može pouzdano da izdvoji ono što ne sme da koristi. Zato podatke filtrira server, a ne agent.
- Rešenja su da server vraća samo podatke potrebne za zadatak i da svaki agent pristupa samo serverima i alatima koji su mu potrebni (načelo najmanjih ovlašćenja). Za podatke o zaposlenima to traži i Zakon o zaštiti podataka o ličnosti, član 5 (minimizacija podataka).
- [[Distribuirano praćenje]] uvećava posledicu, jer trag čuva sve što je agent pročitao. Ovo nije napad: niko ne navodi agenta da iznese podatke, nego server sam daje previše.
