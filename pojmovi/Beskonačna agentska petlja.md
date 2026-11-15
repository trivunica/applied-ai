---
tip: pojam
aliases: [infinite agent loop, infinite loop, step repetition]
izvor: "Cemri, M. i dr. (2025). Why Do Multi-Agent LLM Systems Fail? NeurIPS 2025, Datasets and Benchmarks Track. arXiv:2503.13657, načini otkaza FM-1.3 (step repetition) i FM-1.5 (unaware of termination conditions); Liu, X. i dr. (2024). AgentBench: Evaluating LLMs as Agents. ICLR 2024. arXiv:2308.03688, Task Limit Exceeded"
---
# Beskonačna agentska petlja (infinite agent loop)

## Definicija
Beskonačna agentska petlja je [[Problem|problem]] u kome [[Agentska petlja|agentska petlja]] traje bez napretka: [[AI agent]] ponavlja akcije koje mu ne donose nove rezultate, najčešće iste pozive alata, i ne procenjuje ni da je cilj ostvaren ni da je nedostižan. Takva petlja se završava tek kada je prekine uslov zaustavljanja ili kada se potroše raspoloživi resursi.

## Primer
U drugoj fazi sistema za dijagnostiku kvarova u fabrici [[Orion Precizni Delovi]] operater je prijavio neobičan zvuk sa mašine CNC-04, a rukovodilac održavanja zadao je agentu da utvrdi uzrok. Očitavanja vibracija i temperature bila su u granicama. Agent nije zaključio da se uzrok ne vidi u podacima koje senzori mere, niti je zatražio pregled mašine, nego je ponovo tražio ista očitavanja, zatim evidenciju otkaza, pa opet ista očitavanja. Za dva sata ponovio je iste pozive alata 87 puta i potrošio 1,9 miliona tokena, dok inženjer za AI sisteme nije ručno zaustavio analizu. Uzrok je bio labav zaštitni poklopac, koji senzori na vretenu ne mogu da otkriju. Posle tog slučaja uvedeno je ograničenje od 300.000 tokena po analizi.

## Napomene
- Problem proizlazi iz agentske petlje, koja se završava procenom samog agenta, a ta procena može da izostane. Ponavljanje ne mora da bude doslovno: agent može i da kruži kroz isti niz akcija. Duga petlja nije isto što i beskonačna: u analizi za CNC-09, kojoj je trebalo sedam ciklusa, svaki ciklus je donosio nove podatke.
- Uobičajeno [[Rešenje|rešenje]] je uslov zaustavljanja, na primer najveći broj ciklusa ili tokena, uz prepoznavanje ponovljenih poziva i predaju zadatka čoveku. Ono uvodi nov problem, prerano zaustavljanje: preniska granica prekida i analizu koja napreduje.
- Petlju može da pokrene i [[Istek vremena alata|istek vremena alata]], kada agent ponavlja poziv na koji ne dobija odgovor.
