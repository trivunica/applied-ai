---
tip: pojam
aliases: [data poisoning]
izvor: "NIST AI 100-2e2025, Adversarial Machine Learning: A Taxonomy and Terminology of Attacks and Mitigations, odeljak o napadima trovanjem (poisoning), https://doi.org/10.6028/NIST.AI.100-2e2025; OWASP Top 10 for LLM Applications 2025, LLM04 Data and Model Poisoning"
---
# Trovanje podataka (data poisoning)

## Definicija
Trovanje podataka je [[Problem|problem]] u kome model nauči pogrešno ponašanje iz izmenjenih ili ubačenih podataka za treniranje, jer AI tehnologija ne razlikuje ispravne primere od izmenjenih, nego uči iz svih koje dobije. Podatke najčešće namerno menja napadač, tako da model greši samo u određenim situacijama; napad je okolnost u kojoj se problem javlja, a uzrok je taj [[Nedostatak|nedostatak]].

## Primer
Fabrika [[Orion Precizni Delovi]] angažuje spoljnu firmu da obeleži snimke sa linije za vizuelnu kontrolu. Nezadovoljni radnik te firme obeleži kao ispravne sve snimke kućišta sa ogrebotinom na unutrašnjem prstenu. Model naučen na tim podacima prolazi proveru na ostalim vrstama defekata, ali taj jedan defekt ne prijavljuje.

## Napomene
- Slučajno loše obeleženi podaci nisu trovanje, jer nema napadača. To je problem kvaliteta podataka, iako posledica može biti ista.
- Trovanje se dešava pre upotrebe, pri treniranju. [[Adversarijalni primer]] se dešava tokom upotrebe.
- Teško se otkriva [[Evaluacija|evaluacijom]], jer napadač bira situaciju koju test skup verovatno ne pokriva.
- Rizik raste kada se model automatski [[Ponovno treniranje|ponovo trenira]] na podacima iz rada, jer tada napadač može da utiče na podatke i bez pristupa skupu za treniranje.
