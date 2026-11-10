---
tip: arhitektura
---
# Arhitektura baze znanja

Apstraktna osnova na koju se kače svi pojmovi iz PR-ova. Prati profesorovu tablu, uz naše dodatke (označeni su tako). Svaka beleška u prvoj rečenici navodi rod i linkuje ga. Konvencije termina su u `_meta/odluke.md`.

Izvori navedeni ispod (OECD, AI Act, ISO, NIST) nisu proveravani pretragom. Definicije su nacrti, svaku proveriti da nije preširoka, preuska ili nerazgraničena.

---

## 1. Tabla (izvor istine)

Čitanje fotografije kao ER dijagrama (račva na kraju linije znači "više"):

```
AI Tehnologija ────────< Slučaj korišćenja ────────< Ograničenja
      │                        │         └──────────< Metrike uspeha
      ▼ (više)                 ▼ (više, nije sigurno da je i sa druge strane)
Karakteristika ┈┈┈┈┈┈┈┈┈ Problem ──────────────────── Rešenje
```

- Isprekidana linija Karakteristika i Problem znači da problem proizlazi iz karakteristike.
- Profesor je prvobitno napisao GenAI kao tehnologiju, pa je rekao da se apstrahuje u "AI tehnologija". Generisanje, Analiza i Odlučivanje su dakle vrste (instance) AI tehnologije, a ne zaseban entitet.


---

## 2. Arhitektura

### 2.1 Dijagram

```
 ULAZ ────────▶ AI TEHNOLOGIJA ─────< SLUČAJ KORIŠĆENJA ─┬───< OGRANIČENJE
 Prompt             Generisanje               │          └───< METRIKA USPEHA
 Kontekst modela    Analiza                   │                    ▲ meri
 Modalitet podataka Odlučivanje               │                EVALUACIJA
                      │ 1:N                   │ N:M
                      ▼                       ▼
                KARAKTERISTIKA ┈┈┈┈┈┈┈┈┈┈ PROBLEM ──────────── REŠENJE
                · Mogućnost               · Greška             · Ljudski nadzor
                · Nedostatak              ▼ ima                · može stvoriti nov Problem
                · Neizvesnost             RIZIK
                                          (procena Problema)
```

Legenda:
- Velika slova su krovni pojmovi. Lista ispod čvora (·) su njegove vrste. Izuzetak je "može stvoriti nov Problem" uz Rešenje, to je pravilo, a ne vrsta.
- 7 sa table: AI tehnologija, Karakteristika, Slučaj korišćenja, Ograničenje, Metrika uspeha, Problem, Rešenje.
- Naši dodaci: **Ulaz**, **Rizik**, **Evaluacija**, kao i sve vrste.
- `─────<` znači jedan prema više. `▶` znači "prima" (AI tehnologija prima Ulaz).
- Kontekst (Orion, Lipa) nije čvor osnove, nego okruženje. Sadrži slučajeve korišćenja (vidi odeljak "Slučajevi korišćenja" u Orionu).

### 2.2 Krovni pojmovi (nivo 1, 10 pojmova)

| Čvor | Pitanje na koje odgovara | Nacrt definicije (rod i vrsna razlika) | Na tabli |
|---|---|---|---|
| AI tehnologija | Koja tehnologija? | Sistem koji za zadate ciljeve iz ulaza izvodi izlaz: sadržaj, procenu ili izbor akcije. Izvor (kandidat, proveriti): OECD definicija preuzeta u Uredbu (EU) 2024/1689 čl. 3(1); ISO/IEC 22989 | da |
| Karakteristika | Šta tehnologija može, a šta ne? | Svojstvo AI tehnologije koje određuje šta ona može da uradi u slučaju korišćenja. Vrste: Mogućnost, Nedostatak, Neizvesnost | da |
| Ulaz | Šta tehnologija dobija? | Ono što AI tehnologija prima da bi proizvela izlaz u slučaju korišćenja: podaci, upit ili instrukcija. Vrste: Prompt, Kontekst modela, Modalitet podataka | ne (dodatak) |
| Slučaj korišćenja | Za šta se koristi? | Upotreba AI tehnologije u određenom kontekstu radi ostvarenja cilja, sa zadatim ograničenjima i metrikama uspeha | da |
| Ograničenje | Šta mora da važi? | Andreina definicija: uslov koji alternativa mora da zadovolji da bi bila dozvoljena za izbor | da |
| Metrika uspeha | Kako merimo da je dobro? | Mera kojom se izražava koliko izlaz AI tehnologije ostvaruje cilj slučaja korišćenja | da |
| Problem | Šta može poći naopako? | Neželjeno stanje u slučaju korišćenja koje proizlazi iz neke karakteristike AI tehnologije i narušava ograničenja ili metrike uspeha. Vrsta: Greška | da |
| Rizik | Koliko je to ozbiljno? | Andreina definicija (NIST AI 100-1, ISO 31073): mera koja objedinjuje verovatnoću događaja i veličinu posledica po ciljeve. Procena Problema | ne (dodatak) |
| Rešenje | Šta radimo povodom toga? | Promena AI tehnologije, njenog ulaza ili načina korišćenja u slučaju korišćenja, kojom se smanjuje verovatnoća ili posledica Problema. Alias: mera ublažavanja | da |
| Evaluacija | Kako proveravamo? | Sistematsko merenje koliko izlazi AI tehnologije zadovoljavaju metrike uspeha i ograničenja slučaja korišćenja | ne (dodatak) |

Svaku definiciju proći kroz proveru iz veštine: preširoka, preuska, razgraničena od susednog pojma.

### 2.3 Vrste (nivo 2, 11 pojmova)

| Krovni pojam | Vrste |
|---|---|
| AI tehnologija | **Generisanje sadržaja** (izlaz je nov sadržaj), **Analiza sadržaja** (izlaz je procena svojstva ulaza), **Odlučivanje** (izlaz je izbor akcije) |
| Karakteristika | **Mogućnost**, **Nedostatak**, **Neizvesnost** |
| Ulaz | **Prompt**, **Kontekst modela**, **Modalitet podataka** |
| Problem | **Greška** (izlaz koji narušava ograničenja ili metrike uspeha) |
| Rešenje | **Ljudski nadzor** |

### 2.4 Problem, Greška, Rizik i Rešenje: odluka i raspored

Odluka: **Problem je krovni**. Greška je njegova vrsta. Pojmovi koji nisu Greška (npr. Promena raspodele podataka) vise direktno ispod Problema. Rizik je njegova **procena**, a ne vrsta.

Greška i Rizik ne dele Problem na dva dela, nego odgovaraju na dva različita pitanja:

- **Greška:** šta se već desilo. Izlaz koji krši metriku ili ograničenje.
- **Rizik:** šta može da se desi i koliko košta (verovatnoća puta posledica).
- **Rešenje:** šta radimo povodom toga.

Rizik se računa iz Greške, pa nije njena "sestra". Zato se ne dele pojmovi 50:50, nego svaki pojam ide tamo gde odgovara na svoje pitanje:

| Pojam (PR) | Čvor | Zašto |
|---|---|---|
| Lažno pozitivna i lažno negativna detekcija (#3) | Greška | Izlaz koji krši metriku |
| Halucinacija (#2) | Greška | Uzrok je Nedostatak, sklonost modela |
| Promena raspodele podataka (#3) | Problem | Nije izlaz, nego okolnost koja vodi do grešaka |
| Neuravnoteženost klasa (#3) | Problem | Okolnost u podacima koja vodi do Nedostatka |
| Zamor od upozorenja (#3) | Problem nastao iz Rešenja | Ljudi ignorišu upozorenja |
| Rizik (#1), Cena greške | Rizik | Posledica je deo definicije Rizika |
| Neizvesnost (#1) | Karakteristika | Izvor grešaka i rizika, nije sama rizik |
| Prag odlučivanja (#3) | Rešenje | Granica ocene detekcije. Sidro u osnovi |
| Prag upozorenja (#1) | Rešenje | Granica verovatnoće predikcije (Odlučivanje). Ne spaja se, čeka poglavlje. U napomeni uputiti na Prag odlučivanja |
| Kalibracija modela (#3) | Karakteristika | Postupak kalibrisanja je Rešenje |
| Sintetički podaci (#2) | Rešenje | U drugoj ulozi su izlaz generisanja |
| Ljudski nadzor, Čovek u petlji (#1) | Rešenje | |
| Sistem za uzbunjivanje (#3) | Rešenje | |
| Verifikacija, Validacija, Testiranje (#2) | Vrste Evaluacije | U radu, provera izlaza je i Rešenje |
| Objašnjivost modela (#3) | Mogućnost | Služi Ljudskom nadzoru |

Pravilo: Rešenje može da uvede nov Problem (niži prag smanjuje propuštene otkaze, ali povećava lažne uzbune i zamor).

### 2.5 Ulaz: Prompt i Kontekst

Prompt i Kontekst nemaju mesto na tabli, pa su u ranijim pregledima ostali bez čvora. Nisu ni Karakteristika, ni Problem, ni Rešenje. Odgovaraju na pitanje "šta tehnologija dobija", pa dodajemo **Ulaz**:

- **Prompt** je instrukcija kojom se usmerava generisanje. **Kontekst modela** je sve što model uzima u obzir (Prompt je njegov deo).
- **Modalitet podataka** (#3) je Ulaz za Analizu (slika, tekst, zvuk, vremenska serija).
- Ograničen kontekstni prozor je Nedostatak (Karakteristika). Učenje iz konteksta je Mogućnost.
- Promptovanje i dopuna konteksta su Rešenja: smanjuju halucinacije.
- Naziv: **Kontekst modela** (alias context), da se ne meša sa `konteksti/`.
- Uslovljavanje (#2) je opštiji pojam za nejezičke ulaze (referentna slika, oznaka klase). Čeka poglavlje.

Izlaz nema čvor jer su tri vrste AI tehnologije već podela po izlazu. "Ulaz" i "izlaz" u opštem smislu su pretpostavljeni.

### 2.6 Pravila kačenja pojmova

1. **Rod u prvoj rečenici.** Svaka beleška u prvoj rečenici kaže čija je vrsta i linkuje krovni ili pojam višeg nivoa: "Halucinacija je greška generativne AI tehnologije u kojoj...".
2. **Test pitanja.** Pojam mora da odgovara na bar jedno od pitanja sa table (koja tehnologija, kakve karakteristike, u kom slučaju, koja ograničenja, kako merimo, šta može poći naopako, šta radimo povodom toga). Inače je crna kutija ili van teme.
3. **Crna kutija.** Pojmovi koji opisuju kako tehnologija radi iznutra (Tokenizacija, Embedding, Latentni prostor, arhitekture detektora) nemaju čvor i ne ulaze u osnovu. Za tehnologiju opisujemo ulaz, izlaz i karakteristike, ne unutrašnjost.
4. **Pretpostavljeno.** Pojmovi koje publika zna se upisuju u `_meta/odluke.md`, bez beleške i bez linka.

---

## 3. Sidra (14 postojećih beleški)

**Nivo 1, krovni (10):** AI tehnologija, Karakteristika, Ulaz, Slučaj korišćenja, Ograničenje, Metrika uspeha, Problem, Rizik, Rešenje, Evaluacija.

**Nivo 2, vrste (11):** Generisanje sadržaja, Analiza sadržaja, Odlučivanje, Mogućnost, Nedostatak, Neizvesnost, Prompt, Kontekst modela, Modalitet podataka, Greška, Ljudski nadzor.

**Minimalna osnova = nivo 1 + nivo 2 = 21 beleška.** Arhitektura stoji i bez sidara.

**Nivo 3, sidra (14)**, postojeće beleške uz male izmene, svaka pokazuje po jedan čvor:

| Sidro | PR | Čvor |
|---|---|---|
| Jezički model | #2 | Generisanje sadržaja |
| Veliki jezički model (preimenovati fajl `LLM.md`) | #2 | AI tehnologija, horizontalni pojam koji služi više vrsta |
| Detekcija | #3 | Analiza sadržaja |
| Predikcija | #1 | Izlaz Analize |
| Odluka | #1 | Izlaz Odlučivanja |
| Halucinacija | #2 | Greška |
| Lažno pozitivna detekcija | #3 | Greška |
| Lažno negativna detekcija | #3 | Greška |
| Neuravnoteženost klasa | #3 | Problem |
| Promena raspodele podataka | #3 | Problem |
| Zamor od upozorenja (preimenovati, "alarm") | #3 | Problem nastao iz Rešenja |
| Prag odlučivanja | #3 | Rešenje |
| Čovek u petlji | #1 | Ljudski nadzor |
| Funkcija cilja | #1 | Metrika uspeha |

**Ukupno u PR-u "Osnova": 35 beleški.** Od toga je 22 postojećih (uz izmene) i 13 novih: AI tehnologija, Karakteristika, Ulaz, Slučaj korišćenja, Metrika uspeha, Problem, Rešenje, Generisanje sadržaja, Analiza sadržaja, Odlučivanje, Mogućnost, Nedostatak, Greška.


## 4. Status svih 103 pojma iz PR-ova

Statusi: **OSNOVA** (ulazi u osnovu, uz izmene), **POGLAVLJE** (briše se iz PR-a, obrađuje se u narednim sesijama, ima svoj čvor), **CRNA KUTIJA** (nema čvor, briše se iz PR-a), **PRETPOSTAVLJEN** (ide u `odluke.md`, bez beleške), **SPOJITI ili BRISATI**.

Obrisane beleške ostaju u istoriji commit-ova PR-ova #1, #2 i #3 (grane se ne brišu), pa ništa ne propada. U beleškama osnove se ti pojmovi ne pominju. Popis onoga što se odlaže za naredne sesije je u delu 4 `_meta/arhitektura.md` (statusi POGLAVLJE i CRNA KUTIJA).

### PR #1, odlučivanje (14)

| Pojam | Status | Čvor |
|---|---|---|
| Rizik | OSNOVA | Rizik (krovni) |
| Ograničenje | OSNOVA | Ograničenje (krovni) |
| Neizvesnost | OSNOVA | Karakteristika |
| Ljudski nadzor | OSNOVA | Rešenje |
| Odluka, Predikcija, Čovek u petlji, Funkcija cilja | OSNOVA (sidra) | vidi deo 3 |
| Prag upozorenja | POGLAVLJE | Granica verovatnoće predikcije, vezana za Odlučivanje. Razlikuje se od Praga odlučivanja (#3), koji je granica ocene detekcije |
| Funkcija korisnosti, Optimizacija, Višekriterijumska optimizacija | POGLAVLJE | Odlučivanje, Metrika uspeha |
| Vremenska serija | POGLAVLJE | Modalitet podataka (Ulaz) |
| Prediktivno održavanje | PREMEŠTA SE | u Orion kao slučaj korišćenja, ne kao pojam |

### PR #2, generisanje (29)

| Pojam | Status | Čvor |
|---|---|---|
| Evaluacija | OSNOVA | Evaluacija (krovni), preformulisati |
| Prompt, Kontekst (preimenovati u Kontekst modela) | OSNOVA | Ulaz |
| Halucinacija, Jezički model, LLM | OSNOVA (sidra) | vidi deo 3 |
| Ljudski nadzor | BRISATI | duplikat Andreine beleške (#1) |
| Generativna veštačka inteligencija | SPOJITI | sa vrstom Generisanje sadržaja |
| Model, Podaci, Raspodela, Treniranje, Testiranje | PRETPOSTAVLJEN | |
| Embedding, Latentni prostor, Tokenizacija, Reprezentacija koda | CRNA KUTIJA | |
| Difuzioni model, Generativni dizajn, Generisanje koda, Parametarsko modelovanje, Sintetički podaci | POGLAVLJE | Generisanje (Generativni dizajn se veže na Optimizaciju) |
| Ranjivost | POGLAVLJE | Greška u generisanom kodu |
| Uslovljavanje | POGLAVLJE | Ulaz |
| Reprezentativnost, Statistička vernost | POGLAVLJE | Metrika uspeha (sintetički podaci) |
| Tačnost | POGLAVLJE | Razdvojiti: metrika klasifikacije (Metrika uspeha) i činjenična ispravnost generisanog sadržaja |
| Validacija, Verifikacija | POGLAVLJE | Vrste Evaluacije, uz razgraničenje od skupa za validaciju u ML-u |

### PR #3, analiza (60)

| Pojam | Status | Čvor |
|---|---|---|
| Modalitet podataka | OSNOVA | Ulaz |
| Detekcija, Lažno pozitivna detekcija, Lažno negativna detekcija, Neuravnoteženost klasa, Promena raspodele podataka, Prag odlučivanja, Zamor od upozorenja | OSNOVA (sidra) | vidi deo 3 |
| Nadgledano, Nenadgledano i Polunadgledano učenje, Obeleženi i Neobeleženi podaci, Objekat, Obrazac | PRETPOSTAVLJEN | |
| Autoenkoder, Greška rekonstrukcije, Isolation Forest, One-Class SVM | CRNA KUTIJA | tehnike detekcije anomalija |
| R-CNN, Faster R-CNN, SSD, YOLO, DETR, Dvofazni i Jednofazni detektor, NMS, Granični okvir | CRNA KUTIJA | arhitekture. Popraviti naziv fajla `Grani─ìni okvir.md` pre svake upotrebe |
| Klasifikacija, Detekcija anomalija, Detekcija objekata, Detekcija događaja (tekst, video, zvuk, vreme), Detekcija promena, Detekcija podataka van distribucije, Detekcija zasnovana na pravilima i na udaljenosti, Statistička detekcija anomalija, Detekcija anomalija u vremenskim serijama, Akustička anomalija, Ekstrakcija informacija, Prepoznavanje imenovanih entiteta, Prepoznavanje govora, Događaj, Lokalizacija, Normalno ponašanje | POGLAVLJE | Analiza sadržaja |
| Preciznost, Odziv, F1 mera, Matrica konfuzije, ROC kriva, Kriva preciznosti i odziva, Preklapanje preko unije, Prosečna preciznost, Srednja prosečna preciznost | POGLAVLJE | Metrika uspeha |
| Kalibracija modela, Objašnjivost modela | POGLAVLJE | Karakteristika |
| Sistem za uzbunjivanje | POGLAVLJE | Rešenje |

### Zbir

| Status | Broj |
|---|---|
| OSNOVA (postojeće beleške) | 22 |
| POGLAVLJE | 49 |
| CRNA KUTIJA | 17 |
| PRETPOSTAVLJEN | 12 |
| SPOJITI ili BRISATI | 2 |
| PREMEŠTA SE u kontekst | 1 |
| **Ukupno** | **103** |

Uz to 13 novih beleški. Verovatnoća, Privatnost i slični pojmovi koji se samo linkuju nemaju belešku i pretpostavljeni su.

---

## 5. Test: tri lanca u Orionu

Svaki lanac koristi svih 10 krovnih pojmova. Vrste (11) se koriste bar jednom. Brojke (30%, 25%, 9.200, 2.760, 400) su Andreine, ostalo je ilustrativno.

| Pojam | A. Generisanje: nacrt radne instrukcije | B. Analiza: vizuelna kontrola | C. Odlučivanje: održavanje vretena CNC-07 |
|---|---|---|---|
| AI tehnologija | Generisanje, veliki jezički model | Analiza, detekcija defekata | Odlučivanje nad predikcijom otkaza |
| Ulaz | Prompt (opis dela i mašine), Kontekst modela (tehnička dokumentacija) | Modalitet: slika sa kamera nad izlaznom trakom | Modalitet: vremenska serija vibracija |
| Karakteristika | Mogućnost: piše nacrt iz opisa. Nedostatak: sklonost halucinaciji. Neizvesnost: izlaz je verovatan, ne garantovano tačan | Mogućnost: prepoznaje defekte u realnom vremenu. Nedostatak: slabo prepoznaje retke defekte. Neizvesnost: ocena pouzdanosti | Mogućnost: upozorava dok vreteno još radi. Nedostatak: nekalibrisana procena. Neizvesnost: senzori ne vide unutrašnje stanje ležaja |
| Slučaj korišćenja | Nacrt instrukcije za tehnologa | Vizuelna kontrola delova (kontrolor kvaliteta) | Održavanje vretena CNC-07 (rukovodilac održavanja) |
| Ograničenje | Tehnolog ima ograničeno vreme za pregled | Kontrolor može da proveri ograničen broj upozorenja po smeni | Postoji samo jedno rezervno vreteno |
| Metrika uspeha | Činjenična ispravnost prema dokumentaciji | Odziv na retke defekte i preciznost upozorenja | Funkcija cilja: zbir kazne (zastoj kroz dane kašnjenja), oštećenja alata i preuranjene zamene |
| Problem, Greška | Halucinacija: navedena brzina obrade koja ne postoji u dokumentaciji | Lažno negativna: defektan deo prođe kontrolu | Nastavak rada pri otkazu: propušten otkaz, 6 dana zastoja |
| Rizik | Verovatnoća te greške puta posledica (škart serije) | Reklamacija Kupca A puta verovatnoća propuštenog defekta | 0,3 × 9.200 = 2.760 EUR |
| Rešenje | Ljudski nadzor (tehnolog odobrava), provera simulacijom CNC programa, preciznije promptovanje | Niži prag, sintetički snimci retkih defekata. Nov Problem: zamor od upozorenja | prag od 25% procenjene verovatnoće otkaza, kalibracija, odobrenje rukovodioca (čovek u petlji). Odluka: zamena vretena |
| Evaluacija | Pregled uzorka instrukcija prema dokumentaciji pre puštanja u upotrebu | Test na skupu sa retkim defektima, matrica konfuzije | Poređenje preporuka sa stvarnim otkazima iz evidencije |

Ako neki korak traži pojam koji nije u osnovi, ili taj pojam fali, ili korak spada u poglavlje.

---