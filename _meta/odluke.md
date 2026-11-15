---
tip: odluke
---
# Odluke

## Pretpostavljeni pojmovi
Pojmovi koje publika zna bez definisanja. Nemaju belešku i ne linkuju se. Ne otvaraju se ponovo osim na zahtev studenta.

- aplikacija, baza podataka, API
- verovatnoća, raspodela verovatnoće, očekivana vrednost
- model (mašinskog učenja), podaci, skup podataka, treniranje, testiranje
- nadgledano, nenadgledano i polunadgledano učenje, obeleženi i neobeleženi podaci
- objekat, obrazac, privatnost, ulaz i izlaz (u opštem smislu)
- alat (tool), token, protokol, klijent i server

## Promene konvencija
- 2026-11-09: **Vrste AI tehnologije** se određuju po izlazu: sadržaj, procena svojstva ulaza, izbor akcije. Jedan sistem može biti više vrsta.
- 2026-11-09: **AI tehnologija** ima šire značenje i obuhvata i optimizaciju i pravila. Sintagma "AI rešenje" se ne koristi, piše se "AI tehnologija".
- 2026-11-09: **Crna kutija.** Unutrašnjost modela ne opisujemo, opisujemo ulaz, izlaz i karakteristike.
- 2026-11-09: **Nedostatak** je vrsta Karakteristike. **Ograničenje** je uslov slučaja korišćenja. Engleski *limitation* se ne prevodi kao "ograničenje".
- 2026-11-09: **Odluka** znači samo izbor akcije. Rezultat detekcije ili predikcije nije odluka.
- 2026-11-09: **Jedan zajednički kontekst.** Svi primeri u svim beleškama su u primarnom kontekstu Orion. Poliklinika Lipa je sekundarni kontekst, samo za primere koji ne staju u Orion. Novi slučaj korišćenja se dodaje u odeljak "Slučajevi korišćenja" u Orionu, ne pravi se novi kontekst.
- 2026-11-09: **Kontekst** znači kontekst iz `konteksti/`. Za ulaz modela piše se **Kontekst modela**, a njegova granica je kontekstni prozor.
- 2026-11-09: **Problem** u bazi znači Problem sa profesorove table. Naslov u konfiguraciji je "Odredišni problem".
- 2026-11-09: **Rešenje** je čvor sa table, alias "mera ublažavanja".
- 2026-11-09: **Tačnost** je metrika klasifikacije. Za generisani sadržaj piše se **činjenična ispravnost** (srpski termin nije ustaljen, dogovoriti).
- 2026-11-09: **Raspodela**, ne "distribucija". "Drift" je alias Promene raspodele podataka.
- 2026-11-09: **Upozorenje**, ne "uzbuna" ni "alarm". Zamor od upozorenja (alarm fatigue).
- 2026-11-09: **Greška rekonstrukcije** je skor autoenkodera, ne Greška iz osnove. Dok je crna kutija, ne meša se.
- 2026-11-09: **Nivoi** (krovni, vrste, sidra) umesto slojeva. Slojevi Temelj, Jezgro i Front se ukidaju.
- 2026-11-09: **Rod u prvoj rečenici** svake beleške, sa linkom na rod.
- 2026-11-09: Prag upozorenja (granica verovatnoće predikcije) i Prag odlučivanja (granica ocene detekcije) su dva različita pojma.
- 2026-11-14: **Rod pojma koji nije vrsta krovnog pojma.** Proširuje pravilo o rodu u prvoj rečenici. Ako pojam nije vrsta nijednog krovnog pojma, prva rečenica navodi pretpostavljeni rod i linkuje krovni pojam za koji je pojam vezan. Prvi slučaj je Model Context Protocol: rod je protokol, a vezan je za Ulaz.
- 2026-11-14: **Agentski tok rada** se koristi u užem smislu: putanju koraka unapred zadaje program, a ne model (Anthropic, 2024). Šira upotreba, u kojoj je agentski tok rada svaki višekoračni rad modela (Ng, 2024), pokriva i ono što baza zove AI agent.
- 2026-11-14: **AI agent** se ne naziva autonomnim. Bira korake, a cilj mu zadaje čovek. Po ISO/IEC 22989 (3.1.5) autonoman je sistem koji može da promeni i svoj cilj.
- 2026-11-14: Span se prevodi kao **korak**, a trace kao **trag**.
- 2026-11-14: **Model Context Protocol (MCP)** je vlastito ime i ne prevodi se.
- 2026-11-14: **Distribuirano** u nazivu Distribuirano praćenje znači "kroz više sistema". Nema veze sa raspodelom verovatnoće, pa ne krši konvenciju "raspodela, ne distribucija".
- 2026-11-14: **Pojmovi evaluacije iz teme Agentski AI sistemi** (Veliki jezički model kao evaluator, Praćenje potrošnje tokena, Analiza pojedinačnih koraka) imaju rod Evaluacija. Ulogu Rešenja, kada se primenjuju tokom rada, navode u napomenama, kao i provera izlaza kod Verifikacije i Validacije.
- 2026-11-15: **Istek vremena** (timeout), ne "vremensko ograničenje", jer je Ograničenje u bazi uslov slučaja korišćenja. Sam rok se piše opisno: zadati rok, rok za odgovor.

## Otvorena pitanja
- Srpski termin za "činjenična ispravnost" (factuality) nije ustaljen.
- Kardinalnost Problem i Slučaj korišćenja (N:M) sa table nije sigurna.
- Izvori za AI tehnologiju (OECD, EU AI Act čl. 3, ISO/IEC 22989), Rizik (NIST AI 100-1, ISO 31073), Neizvesnost i Ljudski nadzor treba proveriti pre upisa u `izvor`.
- Prag odlučivanja trenutno pokriva samo ocenu detekcije. Da li ga proširiti na verovatnoću predikcije ili ostaviti Prag upozorenja kao poseban pojam.
- Srpski termin za multi-agent system nije ustaljen: višeagentski ili multiagentski. Baza zasad koristi višeagentski.
- Obrazac orkestrator i izvršioci (orchestrator-workers) Anthropic (2024) svrstava u tokove rada, a po definiciji ove baze bliži je AI agentu, jer model sam deli zadatak.
- Istek vremena alata i Prekomerno izlaganje resursa imaju okidač van AI tehnologije (spor ERP, server koji daje previše podataka) i vise direktno ispod Problema, kao Promena raspodele podataka. Da li za takve probleme uvesti posebnu vrstu Problema?
