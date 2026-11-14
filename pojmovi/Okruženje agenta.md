---
tip: pojam
aliases: [agent harness, agent runtime, okruženje za izvršavanje alata]
izvor: "OpenAI. Function calling, odeljak How it works. https://developers.openai.com/api/docs/guides/function-calling?api-mode=responses"
---
# Okruženje agenta (agent harness)

## Definicija
Okruženje agenta je program koji [[Jezički model|jezičkom modelu]] nudi skup [[Alat|alata]], izvršava [[Poziv alata|pozive alata]] koje model zatraži i vraća modelu podatke o njihovom ishodu.

## Primer
Okruženje asistenta za održavanje u pogonu Orion pre svakog odgovora modela šalje opise ponuđenih alata. Kada model vrati poziv zalihe za CNC-07, okruženje proverava argumente, izvršava upit u ERP-u sa pravima tehničara koji je postavio pitanje i vraća modelu stanje vretena. Model ERP ne vidi i ne poziva ga direktno.

## Napomene
Okruženje je mesto na kome se sprovode provere koje model ne može da garantuje: provera argumenata prema šemi i registru, provera ovlašćenja, ključevi zahteva za ponovljene pozive i [[Sužavanje skupa alata|sužavanje skupa alata]].

U dokumentaciji OpenAI-ja ovu ulogu ima aplikacija (application), a u dokumentaciji za Claude klijent koji izvršava alate.
