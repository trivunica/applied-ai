---
tip: pojam
aliases: [tool call, function call, zahtev za poziv alata]
izvor: "OpenAI. Function calling, odeljak How it works. https://developers.openai.com/api/docs/guides/function-calling?api-mode=responses"
---
# Poziv alata (tool call)

## Definicija
Poziv alata je zahtev [[Jezički model|jezičkog modela]], izražen u njegovom odgovoru, da se izvrši određeni [[Alat|alat]] sa navedenim vrednostima argumenata.

## Primer
Na pitanje tehničara o rezervnom vretenu model u pogonu Orion ne odgovara tekstom, već vraća poziv alata: ime zalihe i argumente masina: „CNC-07” i deo: „vreteno”. Sam poziv ne čita ERP i ne menja ništa u njemu. ERP se čita tek kada [[Okruženje agenta|okruženje agenta]] izvrši poziv.

## Napomene
Kod Claude-a poziv alata je blok tool_use sa poljima id, name i input. Kod OpenAI-ja to je stavka function_call sa poljima call_id, name i arguments.

Poziv alata je zahtev, a ne izvršenje. Izvršenje je posao okruženja agenta, a ono što se posle izvršenja vraća modelu je [[Rezultat alata|rezultat alata]].
