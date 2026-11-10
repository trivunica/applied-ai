---
tip: pojam
aliases: [risk]
izvor: "NIST AI 100-1, Artificial Intelligence Risk Management Framework (AI RMF 1.0), odeljak 1 (Framing Risk); ISO 31073:2022, 3.1.1"
---
# Rizik (risk)

## Definicija
Rizik je procena [[Problem|problema]] AI tehnologije: mera koja objedinjuje verovatnoću da se dogodi neki događaj i veličinu njegovih posledica po ciljeve, a koja postoji zato što je ishod [[Neizvesnost|neizvestan]].

## Primer
Problem koji se ovde procenjuje je [[Greška|greška]] propuštenog otkaza: sistem ne upozori na vreme, a vreteno mašine CNC-07 otkaže tokom rada. Rizik nastavka rada do planiranog servisa u fabrici [[Orion Precizni Delovi]]: događaj je otkaz vretena tokom rada, verovatnoća je 30% u narednih deset dana, a posledice su oštećenje alata od oko 8.000 EUR i zastoj od šest dana, koji donosi ugovornu kaznu za N-2417 od 6 × 200 = 1.200 EUR, ukupno 9.200 EUR. Kao očekivani gubitak to je 0,3 × 9.200 = 2.760 EUR.

## Napomene
- Greška odgovara na pitanje šta se već desilo, a rizik na pitanje koliko je to verovatno i koliko košta. Rizik se računa iz greške, pa nije njena vrsta.
- Veličina posledica (cena greške) je deo definicije rizika, a ne poseban pojam.
- Rizik nije isto što i verovatnoća. Događaj male verovatnoće sa velikim posledicama može nositi veći rizik od česte sitnice.
- Očekivani gubitak (verovatnoća puta posledica) jedan je od načina objedinjavanja, ne jedini. Za retke katastrofalne događaje često nije dovoljan.
- Posledica koja je izvesna nije rizik, jer nema neizvesnosti. Zamena vretena pre servisa je izvestan trošak od 2.300 EUR: 400 EUR kazne za dvodnevno kašnjenje N-2417 i 1.900 EUR za preuranjenu zamenu (neiskorišćeni vek starog vretena). Poređenje sa rizikom nastavka rada (2.760 EUR) pokazuje da se zamena isplati pri verovatnoći otkaza od 30%. Granica isplativosti je 2.300 / 9.200 = 25%.
