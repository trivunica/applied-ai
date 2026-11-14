---
tip: pojam
aliases: [duplicate side effect, dvostruko izvršenje]
izvor: "Jena, J., Dalal, S. The Idempotency-Key HTTP Header Field, IETF Internet-Draft draft-ietf-httpapi-idempotency-key-header. https://datatracker.ietf.org/doc/draft-ietf-httpapi-idempotency-key-header/"
---
# Dupliran efekat poziva (duplicate side effect)

## Definicija
Dupliran efekat poziva je ponovljena promena stanja spoljnog sistema nastala izvršenjem više istovetnih [[Poziv alata|poziva]] [[Alat koji menja stanje|alata koji menja stanje]], kojima je bila nameravana jedna promena.

## Primer
Model u pogonu Orion traži poziv zakazi_servis za CNC-07. ERP upisuje termin, ali se odgovor izgubi zbog prekida veze, a [[Okruženje agenta|okruženju agenta]] istekne vreme čekanja. Okruženje ponavlja isti poziv, ERP ga vidi kao nov zahtev i upisuje drugi termin. U planu održavanja postoje dva termina za istu popravku, iako je svaki pojedinačni poziv bio ispravan.

## Napomene
Uzrok je ponavljanje poziva bez potvrde ishoda prvog pokušaja. Tipični okidači su isteklo vreme čekanja (timeout), prekid veze posle izvršenja i automatsko ponavljanje u okruženju agenta. Kod alata koji samo čitaju dupliran efekat ne nastaje.

Rešenje je opisano u pojmu [[Idempotentan alat]].
