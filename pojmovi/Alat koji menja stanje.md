---
tip: pojam
aliases: [state-changing tool, alat sa sporednim efektom]
izvor: "Fielding, R., Nottingham, M., Reschke, J. RFC 9110: HTTP Semantics, odeljak 9.2.1 Safe Methods. https://www.rfc-editor.org/rfc/rfc9110#section-9.2.1"
---
# Alat koji menja stanje (state-changing tool)

## Definicija
Alat koji menja stanje je [[Alat|alat]] čije izvršenje menja podatke ili tok rada u spoljnom sistemu.

## Primer
U pogonu Orion alat zalihe samo čita stanje delova u ERP-u: ako model pogrešno pročita broj vretena, greška ostaje u odgovoru i ispravlja se novim pozivom. Alat zakazi_servis upisuje termin popravke u plan održavanja i zauzima mašinu CNC-07 i tehničare. Ako se servis zakaže za pogrešan dan, termin ostaje u planu i kada se greška otkrije, sve dok ga neko ne otkaže.

## Napomene
Suprotan pojam je alat koji samo čita, čije izvršenje ne menja stanje spoljnog sistema. Razlika se ne vidi iz oblika opisa, jer oba tipa imaju ime, opis i [[Šema argumenata|šemu argumenata]]; razlika je u posledici greške.

Alat koji, zavisno od argumenata, i čita i menja stanje, kao plan_odrzavanja koji bi i čitao i menjao plan, treba podeliti na dva alata.
