# Runda 1

Miloš Mrđa - Lovac na slepe mrlje

## Prezentacija 1 - Generisanje sadržaja

### 0. Nedostajući pojmovi

> Pojmovi koji su navedeni tokom prezentovanja, ali njihove definicije ne postoje u bazi znanja

- Ograničenje
- Optimizacija
- Simulacija

### 1. Tacnost:

**zamerka:**

> Poenta je da se reč „tačnost“ koristi za dve različite stvari:

> Kod klasifikacije (accuracy) je to konkretna metrika:  
> broj ispravnih predikcija ÷ ukupan broj predikcija.  
> Ako je model ispravno klasifikovao 90 od 100 primera, tačnost mu je 90%.

> Kod generisanog teksta, „tačan“ znači da su tvrdnje u tekstu verne izvoru ili stvarnosti. To nije automatski ista metrika. Sažetak može biti tečan i relevantan, ali da sadrži pogrešan datum ili izmišljenu tvrdnju. Често се проверавају појединачне чињенице у односу на извор, али не постоји један универзалан начин да се израчуна његова „тачност“ као код класификације.

**predlog ispravke:**

```markdown
---
tip: pojam
aliases: [Accuracy]
izvor: "Sokolova, M., Lapalme, G. (2009). A systematic analysis of performance measures for classification tasks. Information Processing & Management, 45(4), 427–437. https://doi.org/10.1016/j.ipm.2009.03.002"
---

# Tačnost klasifikacije (Classification accuracy)

## Definicija

Udeo ispravnih [[Predikcija|predikcija]] [[Klasifikacija|Klasifikacionog]] modela u ukupnom broju predikcija, u odnosu na [[Referentna oznaka|Referentne oznake]].

## Primer

Kamere na liniji za vizuelnu kontrolu u fabrici [[Orion Precizni Delovi]] klasifikuju deo kao ispravan ili neispravan. Od 1.000 delova 10 je neispravnih. Model koji svaki deo proglasi ispravnim ima tačnost 99%, a nijedan neispravan deo ne otkriva.

## Napomene

Visoka tačnost zavara kada su klase neuravnotežene, kao u primeru (Sokolova i Lapalme, 2009). Ne meša se sa [[Činjenična tačnost|činjeničnom tačnošću]] generisanog sadržaja.
```

- Nove zavisnosti. Tačnost klasifikacije koristi pojmove klasifikacija i referentna oznaka, kojih nema u bazi. Treba ih definisati ili pretpostaviti.

---

### 2. Podaci:

**zamerka:**

> Treba jasno razdvojiti podatke za treniranje od ulaza koji se obrađuje pri korišćenju modela.

> Podaci za treniranje služe da se tokom treniranja podese parametri modela. Kod uobičajenog već istreniranog modela, ti podaci nisu ponovo obrađivani za svaki korisnički zahtev.

> Model je naučena matematička funkcija - zajedno sa podešenim parametrima - koja prima ulaz i računa izlaz.

> Ulaz pri korišćenju (inference) je novi podatak na koji se model primenjuje: na primer prompt, slika ili senzorsko očitavanje. Model koristi naučene parametre da bi za taj ulaz napravio predikciju ili generisao odgovor. To samo po sebi ne znači da menja parametre ili uči iz tog zahteva.

**Predlog ispravke:**

```markdown
---
tip: pojam
aliases: [Data]
izvor: "Goodfellow, I., Bengio, Y., Courville, A. (2016). Deep Learning. MIT Press. http://www.deeplearningbook.org"
---

# Trening podaci (Data)

## Definicija

[[Podaci|Podaci]] čijom se obradom tokom [[Treniranje|treniranja]] podešavaju parametri [[Model|modela]].

## Primer

Veliki korpus tekstova na kome se [[Treniranje|trenira]] [[Jezički model|jezički model]].

## Napomene

Pristrasnost u podacima prenosi se na izlaz modela. Nedovoljno raznovrsni podaci daju sadržaj koji slabo pokriva stvarnu raznolikost.
```

---

### 3. Testiranje:

**Zamerka:**

> Ovde se pod „testiranjem“ mogu podrazumevati dve različite provere, pa bi beleška trebalo da kaže na koju misli:

> Testiranje generisanog koda - proverava da li konkretan kod koji je model napravio radi kako je specifikacijom predviđeno. Na primer, testovi pozivaju generisanu funkciju sa različitim ulazima i proveravaju da li vraća očekivane rezultate.

> Testiranje generativnog sistema - proverava kako se sam model ponaša na skupu promptova i uslova. Na primer, da li dosledно prati инструкције, колико су му излази тачни или безбедни и колико резултати варирају између покретања.

> То нису исте ствари: модел може да генерише код који прође своје тестове, али то само по себи не доказује да генеративни систем увек генерише исправан или безбедан код. И обрнуто, добри резултати система на општем тесту не доказују да је одређени генерисани програм исправан.

**Predlog izmene:**

```markdown
---
tip: pojam
aliases: [Testing]
izvor: "Chen, M. i dr. (2021). Evaluating Large Language Models Trained on Code. arXiv:2107.03374. https://arxiv.org/abs/2107.03374"
---

# Testiranje generisanog koda(Testing)

## Definicija

Provera ponašanja konkretnog programa koji je generisao model, pokretanjem unapred definisanih testova sa očekivanim izlazima. Testovi mogu obuhvatiti uobičajene, granične i neispravne ulaze.

## Primer

Za generisanu funkciju piše se skup testova koji proverava rezultate za uobičajene i granične ulaze.

## Napomene

Prolazak testova ne dokazuje da kod nema grešaka, već samo da radi na proverenim slučajevima. Testiranje je jedan od oblika [[Verifikacija|verifikacije]]. Chen i sar. (2021) za ocenu generisanog koda koriste jedinične testove i metriku pass@k, pri čemu je zadatak rešen ako bar jedan od k uzoraka prođe sve testove.
```

---

## Prezentacija 2 - Detekcija

### 1. TP, FP, FN, TN i referentna istina

Ne bih menjao samo jednu rečenicu: dodao bih referentnu istinu i pravilo evaluacije, pa precizirao šta je TP/FP/FN/TN za svaki tip zadatka. Evo predloga teksta koji može direktno u pojmovnik.

```markdown
---
tip: pojam
aliases: [Ground Truth, Gold Standard]
---

# Referentna istina (Ground Truth)

## Definicija

Oznake ili vrednosti koje se za potrebe evaluacije uzimaju kao tačan odgovor. U skupu za testiranje obično ih dodeljuju ljudi prema unapred zadatim smernicama; za detekciju objekata to mogu biti klase i granični okviri, a za vremenske događaje klase i označeni intervali.

## Primer

U fabrici delova kontrolor kvaliteta pregleda 1.000 snimaka delova sa linije za vizuelnu kontrolu i svaki deo označi kao ispravan ili neispravan prema radnoj instrukciji. Označeno je 10 neispravnih delova. Te oznake su referentna istina prema kojoj se ocenjuje model koji klasifikuje delove. Ako je kontrolor propustio neispravan deo, a model ga je prijavio, model će biti ocenjen kao pogrešan iako je u pravu.

## Napomene

Referentna istina je operativna osnova za poređenje predikcija, a ne nužno apsolutno ili nepogrešivo saznanje. Rezultat evaluacije zavisi od potpunosti i doslednosti oznaka, smernica za označavanje i pravila po kojima se predikcije uparuju sa oznakama. Neoznačen primer ne treba automatski smatrati negativnim ako nije potvrđeno da je zaista pregledan i označen kao negativan.
```

**Precizirati pojmove TP, FP, FN i TN**

Možete dodati četiri kratke beleške

```markdown
## Osnovni ishodi evaluacije

Ishodi se određuju poređenjem predikcije sa [[Referentna istina|referentnom istinom]], prema pravilu koje zavisi od zadatka.

- **Tačno pozitivna detekcija (True Positive, TP):** sistem je prijavio traženi primer, a predikcija zadovoljava pravilo poklapanja sa referentnom oznakom.
- **Lažno pozitivna detekcija (False Positive, FP):** sistem je prijavio primer koji nema odgovarajuću referentnu oznaku, ili je prijavio dodatnu predikciju za primer koji je već uparen.
- **Lažno negativna detekcija (False Negative, FN):** referentna oznaka nema odgovarajuću predikciju sistema.
- **Tačno negativna detekcija (True Negative, TN):** jedinica za koju je referentna istina negativna i za koju sistem nije prijavio pozitivnu detekciju.

Šta se smatra primerom, pozitivnom oznakom i odgovarajućom predikcijom mora se definisati za konkretan zadatak. Zato TP, FP, FN i TN nisu određeni samo nazivom metrike.
```

Za beleške Preciznost, Odziv i F1 mera, dodao bih linkove na ove ishode i formule sa jednoznačnim imeniteljima:

```markdown
Preciznost = TP / (TP + FP), odnosno udeo tačnih među svim pozitivnim predikcijama sistema.

Odziv = TP / (TP + FN), odnosno udeo pozitivnih primera iz referentne istine koje je sistem pronašao.

F1 mera = 2 × preciznost × odziv / (preciznost + odziv).
Napomena uz F1: ako su preciznost i odziv obe nula, imenilac je nula; implementacije obično definišu rezultat kao nulu, ali to pravilo treba navesti kada se prijavljuju rezultati.
```

## Prezentacija 3 - Donošenje odluke

### 0. Nedostajući pojmovi

> Pojmovi koji su navedeni tokom prezentovanja, ali njihove definicije ne postoje u bazi znanja

- Model
- Funkcija gubitka
- Očekivani gubitak
- Pareto-optimalnost

### 1. Predikcija

**Zamerka:**

> Definicija je kratka i nije netačna, ali ne razgraničava predikciju od susednih pojmova: Klasifikacija, prognoza, procena verovatnoće

> Ne kaže u kom obliku se predikcija izražava (broj, kategorija ili verovatnoća), pa se ne vidi razlika između predikcije, klasifikacije i procene verovatnoće.

> Ne razlikuje predikciju budućeg događaja (prognozu) od procene trenutno nepoznatog svojstva, na primer ispravnosti dela na snimku. To se pominje tek u napomeni, bez imena tih pojmova.

**Predlog zamerke:**

```markdown
---
tip: pojam
aliases: [prediction]
izvor: "ISO/IEC 22989:2022, Information technology - Artificial intelligence - AI concepts and terminology"
---

# Predikcija (prediction)

## Definicija

Procena vrednosti ili ishoda koji nije poznat u trenutku odlučivanja, koju [[Model|model]] izračunava iz [[Podaci|podataka]], izražena kao broj, kategorija ili verovatnoća.

## Primer

Iz [[Vremenska serija|vremenske serije]] vibracija vretena mašine CNC-07 model u fabrici delova procenjuje da će vreteno otkazati u narednih deset dana sa verovatnoćom 30%. Procena nije odluka: rukovodilac održavanja na osnovu nje tek bira šta će uraditi.

## Napomene

- Oblik predikcije zavisi od zadatka: broj (očekivana jačina vibracija vretena sutra), kategorija (deo na snimku je ispravan ili neispravan) ili verovatnoća (30% otkaza u narednih deset dana). Predikcija u obliku kategorije je klasifikacija.
- Predikcija se ne odnosi samo na budućnost. Kamere na liniji vizuelne kontrole predviđaju da li je deo ispravan, što je trenutno nepoznato svojstvo dela koji već postoji. Predikcija buduće vrednosti ili događaja je prognoza i često se izvodi iz vremenske serije.
- Predikcija je ulaz u [[Odluka|odluku]], ali nije svaka odluka zasnovana na predikciji.
- Broj koji model vrati (na primer 85%) ne mora biti prava verovatnoća. Ako je model kalibrisan, među mnogo slučajeva kojima dodeli oko 85% ishod se dogodi u oko 85% slučajeva. Kalibracija se proverava na podacima koji nisu korišćeni za treniranje.
- Svaka predikcija nosi [[Neizvesnost|neizvesnost]].
```
