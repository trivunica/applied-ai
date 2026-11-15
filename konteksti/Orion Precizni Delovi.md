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
- **ERP sistem**: proizvodni nalozi, zalihe, nabavka, fakture, ugovori, troškovi proizvodnje i kadrovska evidencija.
- **Sistem za prediktivno održavanje**: iz senzorskih očitavanja procenjuje verovatnoću otkaza vretena u narednih deset dana i predlaže intervenciju.
- **Linija za vizuelnu kontrolu**: kamere nad izlaznom trakom.
- **Sistem za tehničku dokumentaciju**: crteži, radne instrukcije i CNC programi koje priprema tehnolog, kao i dokumentacija proizvođača mašina (dozvoljene vrednosti vibracija, procedure zamene vretena).
- **Sistem za dijagnostiku kvarova**: na zahtev rukovodioca održavanja utvrđuje verovatan uzrok kvara mašine i priprema nacrt servisnog naloga. Uveden je u tri faze: prvo kao agentski tok rada sa fiksnim koracima, zatim kao jedan AI agent koji sam bira korake, a sada radi kao višeagentski sistem sa koordinacionim agentom i tri agenta (za senzorske podatke, za tehničku dokumentaciju i za troškove).
- **MCP serveri**: posrednici preko kojih sistem za dijagnostiku kvarova pristupa ERP sistemu, sistemu za prikupljanje senzorskih podataka i sistemu za tehničku dokumentaciju.
- **Platforma za praćenje AI agenata (Arize Phoenix)**: beleži tragove izvršavanja sistema za dijagnostiku kvarova, potrošnju tokena i rezultate evaluacije.
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
- Servisni nalozi: opis kvara, verovatan uzrok, procedura popravke, potrebni delovi, procenjeni trošak i rok. Nacrt priprema sistem za dijagnostiku kvarova, a nalog odobrava rukovodilac održavanja. Nalog čitaju i operateri koji učestvuju u popravci.
- Kadrovska evidencija (podaci o zaposlenima, uključujući zarade) i troškovi proizvodnje po nalogu i mašini.
- Tragovi izvršavanja sistema za dijagnostiku kvarova: koraci, ulazi i izlazi poziva modela i alata, trajanje i potrošnja tokena.

### Ljudi i uloge
- Rukovodilac održavanja.
- Planer proizvodnje (nedeljni raspored naloga po mašinama, ponedeljkom).
- Operateri mašina. Sertifikat se stiče po tipu mašine: za tip CNC-07 i CNC-09 imaju ga troje operatera, a u drugoj smeni radi samo jedan od njih.
- Tehnolog.
- Kontrolor kvaliteta.
- Referent nabavke.
- Referent ugovora.
- Direktor proizvodnje.
- Inženjer za AI sisteme: održava sistem za dijagnostiku kvarova i MCP servere i prati njihov rad na platformi za praćenje.

### Procesi
- Planiranje proizvodnje (nedeljno).
- Obrada na CNC mašinama u dve smene po 8 sati, pet dana nedeljno.
- Kontrola kvaliteta.
- Održavanje: planirani servis po rasporedu (za CNC-07 za deset dana) i interventno.
- Nabavka sirovine.
- Isporuka kupcima.
- Mesečni obračun zarada u ERP sistemu, tokom koga ERP sporo odgovara na upite.

### Pravila i ograničenja
- Mašina u jednom trenutku obrađuje najviše jedan nalog.
- Ugovorna kazna za kašnjenje iznosi 0,5% vrednosti naloga po danu kašnjenja (N-2417: 200 EUR dnevno, N-2420: 500 EUR dnevno).
- Operater mora imati sertifikat za tip mašine koju opslužuje.

### Spoljni subjekti
- Kupac A (proizvođač automobilskih komponenti) i drugi kupci.
- Dobavljač čelika.
- Servisna firma za vretena.
- Snabdevač električnom energijom, koji dodatno naplaćuje vršnu potrošnju.

## Slučajevi korišćenja
Svaki slučaj je upotreba AI tehnologije u ovoj fabrici radi zadatog cilja. Na njima se testira cela arhitektura (`_meta/arhitektura.md`). Novi slučaj se dodaje ovde, ne u novi kontekst.

### Nacrt radne instrukcije (generisanje sadržaja)
Tehnolog dobija od jezičkog modela nacrt radne instrukcije za novi deo na osnovu opisa dela, mašine i tehničke dokumentacije, pa ga pregleda i odobrava.
- Korisnik: tehnolog.
- Ograničenje: tehnolog ima ograničeno vreme za pregled.
- Metrika uspeha: činjenična ispravnost nacrta prema tehničkoj dokumentaciji.

### Vizuelna kontrola delova (analiza sadržaja)
Kamere nad izlaznom trakom snimaju delove, a sistem otkriva defekte i prijavljuje ih kontroloru kvaliteta.
- Korisnik: kontrolor kvaliteta.
- Ograničenje: kontrolor može da proveri ograničen broj upozorenja po smeni.
- Metrika uspeha: odziv na retke defekte i preciznost upozorenja.

### Prediktivno održavanje vretena (odlučivanje)
Sistem za prediktivno održavanje procenjuje verovatnoću otkaza vretena CNC-07 u narednih deset dana, a rukovodilac održavanja bira da li da vreteno zameni pre planiranog servisa ili da nastavi rad.
- Korisnik: rukovodilac održavanja.
- Ograničenje: u skladištu postoji samo jedno rezervno vreteno za taj tip.
- Metrika uspeha: funkcija cilja, odnosno zbir ugovornih kazni (zastoj se iskazuje kroz dane kašnjenja), oštećenja alata i troška preuranjene zamene vretena.

### Dijagnostika kvara i priprema servisnog naloga (agentski AI sistem)
Kada sistem za prediktivno održavanje upozori na rizik otkaza ili operater prijavi kvar, rukovodilac održavanja zadaje sistemu za dijagnostiku kvarova da utvrdi verovatan uzrok i pripremi nacrt servisnog naloga. Sistem sam prikuplja očitavanja, tehničku dokumentaciju, evidenciju otkaza i servisa i stanje zaliha, a rukovodilac pregleda nacrt i odobrava nalog.
- Korisnik: rukovodilac održavanja.
- Ograničenja: sistem sme samo da čita podatke, i to samo one potrebne za dijagnostiku; nalog postaje važeći tek kada ga rukovodilac odobri; jedna analiza sme da potroši najviše 300.000 tokena.
- Metrike uspeha: tehnička ispravnost dijagnoze i predložene procedure prema tehničkoj dokumentaciji i evidenciji otkaza; broj tokena potrošenih po analizi.
