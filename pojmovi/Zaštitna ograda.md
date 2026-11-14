---
tip: pojam
aliases: [guardrail]
izvor: "nije pronađen standardni izvor; termin je ustaljen u industriji"
---
# Zaštitna ograda (guardrail)

## Definicija
Zaštitna ograda je [[Rešenje|rešenje]] u kome se [[Ulaz|ulaz]] ili izlaz AI tehnologije automatski proverava prema unapred zadatim pravilima. Izlaz koji krši pravilo se blokira, ispravlja ili prosleđuje čoveku pre nego što se upotrebi.

## Primer
Pre nego što nacrt radne instrukcije stigne do tehnologa u fabrici [[Orion Precizni Delovi]], program iz nacrta izdvaja sve brzine obrade i poredi ih sa dozvoljenim opsegom iz tehničke dokumentacije za taj tip mašine. Ako jezički model navede brzinu izvan opsega, kao kod [[Halucinacija|halucinacije]], nacrt se ne prosleđuje dalje, a tehnolog dobija označeno sporno mesto.

## Napomene
- Razlika od [[Ljudski nadzor|ljudskog nadzora]]: zaštitna ograda je automatska i proverava samo ono što pravilo pokriva. Čovek može da uoči i ono što niko nije predvideo.
- Pravila moraju biti proverljiva bez modela (opseg, format, zabranjene reči, dozvoljeni alati). Kada proveru radi drugi model, to je druga tehnika sa sopstvenim greškama.
- Smanjuje, ali ne uklanja [[Ubacivanje instrukcija|ubacivanje instrukcija]], jer napadač može da formuliše instrukciju koju pravila ne prepoznaju.
- Svako blokiranje je i upozorenje, pa previše strogih pravila vodi u [[Zamor od upozorenja|zamor od upozorenja]].
