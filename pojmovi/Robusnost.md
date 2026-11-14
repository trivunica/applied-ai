---
tip: pojam
aliases: [robustness]
izvor: "NIST AI 100-1, Artificial Intelligence Risk Management Framework (AI RMF 1.0), odeljak 3.1 (Valid and Reliable), https://doi.org/10.6028/NIST.AI.100-1"
---
# Robusnost (robustness)

## Definicija
Robusnost je [[Karakteristika|karakteristika]] AI tehnologije: sposobnost da zadrži nivo [[Metrika uspeha|metrika uspeha]] i kada se [[Ulaz|ulaz]] razlikuje od ulaza na kojima je proverena, bilo zbog prirodnih promena okruženja, bilo zbog namerne izmene ulaza.

## Primer
Sistem za vizuelnu kontrolu u fabrici [[Orion Precizni Delovi]] proveren je na snimcima iz prve smene, pri dnevnom svetlu. U drugoj smeni hala je osvetljena samo reflektorima, pa delovi na snimcima imaju jače odsjaje. Ako sistem i tada otkriva isti udeo defekata kao danju, robustan je na promenu osvetljenja. Ako odziv na defekte noću padne sa 95% na 70%, nije, i to je njegov [[Nedostatak|nedostatak]].

## Napomene
- Razlikuju se dve vrste robusnosti: na prirodne promene ulaza (osvetljenje, novi dobavljač, habanje senzora) i na namerne izmene ([[Adversarijalni primer|adversarijalni primer]]). Sistem može imati jednu, a nemati drugu.
- Robusnost nije isto što i tačnost. Tačnost se meri na jednom skupu podataka, a robusnost pokazuje koliko se ta mera menja kada se ulazi promene.
- Nedostatak robusnosti je uzrok kojem [[Problem|problemi]] kao što su [[Promena raspodele podataka|promena raspodele podataka]] i adversarijalni primer daju posledice.
