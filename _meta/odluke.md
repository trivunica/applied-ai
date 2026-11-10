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

## Otvorena pitanja
- Srpski termin za "činjenična ispravnost" (factuality) nije ustaljen.
- Kardinalnost Problem i Slučaj korišćenja (N:M) sa table nije sigurna.
- Izvori za AI tehnologiju (OECD, EU AI Act čl. 3, ISO/IEC 22989), Rizik (NIST AI 100-1, ISO 31073), Neizvesnost i Ljudski nadzor treba proveriti pre upisa u `izvor`.
- Prag odlučivanja trenutno pokriva samo ocenu detekcije. Da li ga proširiti na verovatnoću predikcije ili ostaviti Prag upozorenja kao poseban pojam.
