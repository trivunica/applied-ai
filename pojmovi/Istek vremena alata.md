---
tip: pojam
aliases: [MCP tool timeout, tool timeout, timeout]
izvor: "Model Context Protocol Specification, revizija 2026-07-28: Tools (Security Considerations, Error Handling) i Cancellation (Timeouts). https://modelcontextprotocol.io/specification/2026-07-28/basic/patterns/cancellation"
---
# Istek vremena alata (tool timeout)

## Definicija
Istek vremena alata je [[Problem|problem]] u kome poziv alata koji je uputio [[AI agent]] ne dobije odgovor u zadatom roku, pa se poziv prekida, a agent ostaje bez rezultata na osnovu koga je trebalo da izabere sledeću akciju.

## Primer
Agent za troškove u sistemu za dijagnostiku kvarova fabrike [[Orion Precizni Delovi]] preko MCP servera ispred ERP sistema poziva alat za stanje zaliha, da proveri da li je rezervno vreteno za CNC-07 na stanju. ERP sistem tada radi mesečni obračun zarada i ne odgovara, pa MCP klijent posle zadatih 30 sekundi prekida poziv. Agent nastavlja bez tog podatka i u nacrt servisnog naloga upisuje da je vreteno na stanju, iako je jedino rezervno vreteno tog tipa nedelju dana ranije ugrađeno u CNC-09. Nacrt ne pokazuje da zalihe nisu proverene, pa ga rukovodilac održavanja odobrava sa rokom zamene od dva dana. Vreteno zatim mora da se naruči, nalog N-2417 kasni pet dana više, a ugovorna kazna raste za 1.000 EUR.

## Napomene
- Rok za odgovor je i sam [[Rešenje|rešenje]]: bez njega bi agent čekao odgovor koji možda nikada ne stiže. Istek vremena je problem koji to rešenje uvodi. U MCP-u rok postavlja klijent, a specifikacija preporučuje da ga ima svaki zahtev.
- Šta sledi posle isteka zavisi od [[Agentska petlja|agentske petlje]], jer agent sledeću akciju bira na osnovu rezultata prethodne. Ako ponavlja isti poziv, nastaje [[Beskonačna agentska petlja|beskonačna agentska petlja]]. Ako nedostajući podatak zameni pretpostavkom, kao u primeru, nastaje [[Halucinacija|halucinacija]].
- Posledicu smanjuje to da agent dobije jasnu poruku da je poziv istekao, da broj ponovnih pokušaja ograniči program, a ne model, i da nacrt naloga označi podatke koji nisu provereni, kako bi ih rukovodilac proverio ([[Ljudski nadzor|ljudski nadzor]]).
