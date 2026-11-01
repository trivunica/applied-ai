---
tip: pojam
aliases: [utility function]
izvor: "Russell i Norvig, Artificial Intelligence: A Modern Approach (4. izd.), poglavlje Making Simple Decisions"
---
# Funkcija korisnosti (utility function)

## Definicija
Funkcija koja svakom mogućem ishodu [[Odluka|odluke]] dodeljuje broj koji izražava njegovu poželjnost za donosioca odluke, tako da veći broj označava poželjniji ishod.

## Primer
Rukovodilac održavanja ocenjuje ishode odluke o mašini CNC-07 na skali od 0 do 100: vreteno zamenjeno odmah, nalog kasni dva dana: 70. Vreteno izdrži do planiranog servisa: 95. Vreteno otkaže tokom rada, zastoj šest dana i oštećen alat: 10. Pošto model procenjuje 30% verovatnoće otkaza ako se nastavi rad, očekivana korisnost nastavka je 0,7 × 95 + 0,3 × 10 = 69,5, što je nešto manje od 70 za zamenu odmah.

## Napomene
- Pri [[Neizvesnost|neizvesnosti]] akcija se vrednuje očekivanom korisnošću: zbir korisnosti mogućih ishoda ponderisanih njihovim verovatnoćama.
- [[Funkcija cilja|Funkcija cilja]] ocenjuje alternative, a funkcija korisnosti ishode. Kada je ishod svake alternative izvestan, obe se mogu poklopiti (na primer korisnost kao negativan trošak).
- Brojevi korisnosti izražavaju preferencije donosioca odluke i nisu merljivi kao trošak u evrima. Dva donosioca odluke mogu imati različite funkcije korisnosti za iste ishode.
