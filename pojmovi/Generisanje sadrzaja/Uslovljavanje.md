---
tip: pojam
aliases: [Conditioning]
izvor: "Rombach, R. i dr. (2022). High-Resolution Image Synthesis with Latent Diffusion Models. CVPR 2022, str. 10684–10695. https://arxiv.org/abs/2112.10752"
---
# Uslovljavanje (Conditioning)

## Definicija
Usmeravanje generisanja dodatnim ulazom, kao što su tekstualni opis ([[Prompt]]), oznaka klase ili referentna slika, tako da izlaz odgovara zadatom uslovu.

## Primer
Isti [[Difuzioni model]] dobija opis „zimski pejzaž“ i generiše sliku sa snegom.

## Napomene
Uslovljavanje ne garantuje da će svaki element opisa biti ispoštovan; broj objekata i njihovi odnosi često su pogrešni. Rombach i sar. (2022) uvode slojeve unakrsne pažnje (cross-attention) za uslovljavanje, na primer tekstom ili okvirima objekata (bounding box).
