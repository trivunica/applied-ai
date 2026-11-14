---
tip: pojam
aliases: [idempotent tool, idempotentnost, ključ zahteva, idempotency key]
izvor: "Fielding, R., Nottingham, M., Reschke, J. RFC 9110: HTTP Semantics, odeljak 9.2.2 Idempotent Methods. https://www.rfc-editor.org/rfc/rfc9110#section-9.2.2"
---
# Idempotentan alat (idempotent tool)

## Definicija
Idempotentan alat je [[Alat|alat]] kod koga izvršenje više istovetnih [[Poziv alata|poziva]] ostavlja spoljni sistem u istom stanju kao izvršenje jednog poziva.

## Primer
[[Okruženje agenta|Okruženje agenta]] u pogonu Orion pre prvog izvršenja poziva zakazi_servis za CNC-07 dodeljuje mu ključ srv-07-4471. ERP upisuje termin i čuva ključ zajedno sa rezultatom. Odgovor se izgubi i okruženje ponavlja poziv sa istim ključem. ERP prepoznaje ključ, ne upisuje nov termin i vraća sačuvani rezultat. U planu održavanja ostaje jedan termin, bez obzira na broj ponavljanja.

## Napomene
Ključ zahteva (idempotency key) je jedinstvena oznaka koju klijent dodeljuje zahtevu da bi alat prepoznao ponovljeno slanje istog zahteva. Ključ generiše okruženje agenta pre prvog pokušaja, a ne model u argumentima poziva, jer bi model pri ponavljanju mogao da napravi nov ključ. Ključ se vezuje za konkretan zahtev, a ne za mašinu: novi servis za CNC-07 sledećeg meseca dobija nov ključ.

Primer implementacije je Stripe API: čuva ključ i rezultat, vraća grešku ako isti ključ stigne sa drugim parametrima i ključeve uklanja posle najmanje 24 sata. Problem koji idempotentnost rešava opisan je u pojmu [[Dupliran efekat poziva]].
