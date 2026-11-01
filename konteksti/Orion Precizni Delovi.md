---
tip: kontekst
uloga: primarni
---
# Orion Precizni Delovi

Orion Precizni Delovi je izmišljena srednja fabrika (oko 120 zaposlenih) koja preciznom obradom metala izrađuje kućišta ležajeva i zupčanike za kupce iz automobilske industrije. Pogodna je za ilustraciju primene AI jer ima opremu sa senzorima, proizvodne naloge sa rokovima i ugovornim kaznama, ograničene resurse i zalihe, tehničku dokumentaciju i ugovore, pa se u njoj javljaju generisanje sadržaja, analiza sadržaja i odlučivanje. Sve brojke u primerima su izmišljene.

## Elementi

### Sistemi
- **CNC mašine**: 12 CNC strugova i glodalica, oznake CNC-01 do CNC-12. CNC-07 i CNC-09 su iste serije (vretena istog tipa). Rezervno vreteno za taj tip nalazi se u skladištu.
- **Sistem za prikupljanje senzorskih podataka**: senzori vibracija i temperature na vretenima, očitavanja u kratkim intervalima.
- **Sistem za praćenje proizvodnje**: beleži stanje mašina i napredak naloga.
- **ERP sistem**: proizvodni nalozi, zalihe, nabavka, fakture, ugovori.
- **Sistem za prediktivno održavanje**: iz senzorskih očitavanja procenjuje verovatnoću otkaza vretena u narednih deset dana i predlaže intervenciju.
- **Linija za vizuelnu kontrolu**: kamere nad izlaznom trakom.
- **Sistem za tehničku dokumentaciju**: crteži, radne instrukcije i CNC programi koje priprema tehnolog.
- **Autonomno transportno vozilo (AGV)**: prevozi palete između skladišta i mašina.
- **Skladište**: sirovina (čelične šipke) i gotovih delova.
- **Brojila električne energije**: po proizvodnim halama.

### Podaci
- Očitavanja vibracija i temperature po mašini.
- Evidencija otkaza i servisa.
- Proizvodni nalozi (količina, vrednost, rok, kupac). Primeri: N-2417 (500 kućišta ležaja za Kupca A, vrednost 40.000 EUR) i N-2420 (vrednost 100.000 EUR).
- Stanje zaliha čelika.
- Potrošnja električne energije po satima.
- Ugovori sa kupcima i dobavljačima, uključujući klauzule o ugovornim kaznama.
- Fakture dobavljača.
- Snimci kamera sa linije za vizuelnu kontrolu.
- Radne instrukcije i CNC programi.

### Ljudi i uloge
- Rukovodilac održavanja.
- Planer proizvodnje (nedeljni raspored naloga po mašinama, ponedeljkom).
- Operateri mašina. Sertifikat se stiče po tipu mašine: za tip CNC-07 i CNC-09 imaju ga troje operatera, a u drugoj smeni radi samo jedan od njih.
- Tehnolog.
- Kontrolor kvaliteta.
- Referent nabavke.
- Referent ugovora.
- Direktor proizvodnje.

### Procesi
- Planiranje proizvodnje (nedeljno).
- Obrada na CNC mašinama u dve smene po 8 sati, pet dana nedeljno.
- Kontrola kvaliteta.
- Održavanje: planirani servis po rasporedu (za CNC-07 za deset dana) i interventno.
- Nabavka sirovine.
- Isporuka kupcima.

### Pravila i ograničenja
- Mašina u jednom trenutku obrađuje najviše jedan nalog.
- Ugovorna kazna za kašnjenje iznosi 0,5% vrednosti naloga po danu kašnjenja (N-2417: 200 EUR dnevno, N-2420: 500 EUR dnevno).
- Operater mora imati sertifikat za tip mašine koju opslužuje.

### Spoljni subjekti
- Kupac A (proizvođač automobilskih komponenti) i drugi kupci.
- Dobavljač čelika.
- Servisna firma za vretena.
- Snabdevač električnom energijom, koji dodatno naplaćuje vršnu potrošnju.
