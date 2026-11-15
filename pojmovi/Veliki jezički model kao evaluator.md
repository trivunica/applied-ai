---
tip: pojam
aliases: [LLM-as-a-judge, LLM judge, LLM evaluator]
izvor: "Zheng, L. i dr. (2023). Judging LLM-as-a-Judge with MT-Bench and Chatbot Arena. NeurIPS 2023, Datasets and Benchmarks Track. arXiv:2306.05685"
---
# Veliki jezički model kao evaluator (LLM-as-a-judge)

## Definicija
Veliki jezički model kao evaluator je vrsta [[Evaluacija|evaluacije]] u kojoj [[Veliki jezički model|veliki jezički model]] ocenjuje izlaze AI tehnologije prema kriterijumima zadatim u [[Prompt|promptu]], umesto da ih ocenjuje čovek ili unapred napisana formula.

## Primer
Posle slučaja u kome je nacrt servisnog naloga tvrdio da je rezervno vreteno na stanju iako zalihe nisu proverene (vidi [[Istek vremena alata]]), platforma za praćenje u fabrici [[Orion Precizni Delovi]] svaki nacrt, zajedno sa tragom analize, daje velikom jezičkom modelu kao evaluatoru. U promptu su dva kriterijuma izvedena iz metrike uspeha slučaja korišćenja: da li se procedura zamene vretena u nacrtu slaže sa dokumentacijom proizvođača mašine i da li je svaka tvrdnja u nacrtu potkrepljena rezultatom nekog poziva alata iz traga. Za svaki kriterijum evaluator vraća ocenu "ispravno" ili "neispravno" uz kratko obrazloženje. Nacrt iz tog slučaja sada bi po drugom kriterijumu dobio ocenu "neispravno", jer u tragu nema rezultata koji potkrepljuje tvrdnju o zalihama. Pre uvođenja evaluatora inženjer za AI sisteme uporedio je njegove ocene sa ocenama rukovodioca održavanja na 50 ranijih naloga, i one su se poklopile u 43 slučaja.

## Napomene
- Evaluator je i sam AI tehnologija, pa i on greši. Poznate su tri pristrasnosti: kada poredi dva odgovora, daje prednost onom koji je naveden prvi; daje prednost dužem odgovoru; daje prednost odgovorima sopstvenog modela. Zato se pre upotrebe proverava koliko se njegove ocene slažu sa ocenama ljudi, kao u primeru.
- Kada ocenjuje nacrt pre nego što ga vidi čovek, evaluator je i [[Rešenje|rešenje]]: nacrt ocenjen kao neispravan vraća se agentu ili stiže rukovodiocu održavanja sa upozorenjem. [[Ljudski nadzor]] time ne prestaje, jer nalog i dalje odobrava rukovodilac.
- Formula meri ono što se može izbrojati, kao u [[Praćenje potrošnje tokena|praćenju potrošnje tokena]], a evaluator ono što traži razumevanje teksta, kao što je slaganje procedure sa dokumentacijom.
