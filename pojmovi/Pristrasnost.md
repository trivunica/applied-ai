---
tip: pojam
aliases: [bias, harmful bias]
izvor: "NIST SP 1270, Towards a Standard for Identifying and Managing Bias in Artificial Intelligence (2022), https://doi.org/10.6028/NIST.SP.1270"
---
# Pristrasnost (bias)

## Definicija
Pristrasnost je [[Problem|problem]] AI tehnologije u kome izlaz za neku grupu ulaza (mašina, delova, ljudi) sistematski odstupa od ispravnog, jer podaci ili način na koji je model naučen tu grupu ne predstavljaju verno.

## Primer
Sistem za prediktivno održavanje u fabrici [[Orion Precizni Delovi]] naučen je na evidenciji otkaza u kojoj je najviše zapisa sa mašina CNC-01 do CNC-06. Mašine CNC-07 i CNC-09 su druge serije, sa drugačijim vretenima, i u evidenciji imaju samo nekoliko otkaza. Sistem zato za njih procenjuje verovatnoću otkaza sistematski niže nego što jeste, pa rukovodilac održavanja dobija upozorenje za CNC-07 kasnije nego za ostale mašine.

## Napomene
- Ključna reč je *sistematski*. Pojedinačna [[Greška|greška]] nije pristrasnost. Pristrasnost je kada greške za jednu grupu idu u istom smeru.
- Ovo nije statistička pristrasnost procenjivača (bias–variance), iako se na engleskom isto zove.
- [[Neuravnoteženost klasa]] je okolnost u podacima (malo primera jedne klase izlaza) koja može da dovede do pristrasnosti. Pristrasnost se odnosi na grupe ulaza, ne na klase izlaza.
- Preterano oslanjanje čoveka na izlaz sistema (automation bias) je ljudska, a ne modelska pristrasnost. Pominje se u [[Ljudski nadzor|ljudskom nadzoru]].
