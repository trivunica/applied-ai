---
tip: pojam
aliases: [duplicate side effect, dvostruko izvršenje]
izvor: "Jena, J., Dalal, S. The Idempotency-Key HTTP Header Field, IETF Internet-Draft draft-ietf-httpapi-idempotency-key-header. https://datatracker.ietf.org/doc/draft-ietf-httpapi-idempotency-key-header/"
---
# Dupliran efekat poziva (duplicate side effect)

## Definicija
Dupliran efekat poziva je ponovljena promena stanja spoljnog sistema nastala izvršenjem više istovetnih [[Poziv alata|poziva]] [[Alat koji menja stanje|alata koji menja stanje]], kojima je bila nameravana jedna promena.

## Primer
Model u pogonu Orion traži poziv zakazi_servis za CNC-07. ERP upisuje termin, ali se odgovor izgubi zbog prekida veze, a [[Okruženje agenta|okruženje agenta]] beleži [[Istek vremena alata|istek vremena alata]]. Okruženje ponavlja isti poziv, ERP ga vidi kao nov zahtev i upisuje drugi termin. U planu održavanja postoje dva termina za istu popravku, iako je svaki pojedinačni poziv bio ispravan.

## Napomene
Uzrok je ponavljanje poziva bez potvrde ishoda prvog pokušaja. Tipični okidači su [[Istek vremena alata|istek vremena alata]], prekid veze posle izvršenja i automatsko ponavljanje u okruženju agenta. Istek vremena ne znači da poziv nije izvršen, već da njegov ishod nije poznat.

Ponavljanje posle isteka vremena je bezbedno u dva slučaja: kada alat samo čita i kada je alat [[Idempotentan alat|idempotentan]], a ponovljeni poziv nosi isti ključ zahteva. Kod alata koji menja stanje, a nije idempotentan, okruženje agenta pre ponavljanja proverava stanje sistema, na primer da li termin za CNC-07 već postoji, ili poziv ne ponavlja i prijavljuje nepoznat ishod.
