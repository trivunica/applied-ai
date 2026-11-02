---
tip: pojam
aliases: [Latent space]
izvor: "Rombach, R. i dr. (2022). High-Resolution Image Synthesis with Latent Diffusion Models. CVPR 2022, str. 10684–10695. https://arxiv.org/abs/2112.10752"
---
# Latentni prostor (Latent space)

## Definicija
Sažeta numerička reprezentacija u kojoj se sadržaj (na primer slika) opisuje svojim ključnim obeležjima. U latentnim difuzionim modelima slika se najpre kodira pomoću unapred treniranog autoenkodera, a generisanje se odvija u tom prostoru, a ne nad pikselima.

## Primer
[[Difuzioni model]] ne obrađuje svaki piksel, već radi nad sažetom reprezentacijom slike, što ubrzava generisanje.

## Napomene
Latentni prostor je blizak pojmu [[Embedding|embeddinga]], ali nije isto: embedding je konkretan vektor, a latentni prostor je prostor u kome takvi vektori žive.
