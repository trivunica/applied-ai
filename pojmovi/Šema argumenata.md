---
tip: pojam
aliases: [argument schema, input schema, parameters]
izvor: "OpenAI. Function calling. https://developers.openai.com/api/docs/guides/function-calling?api-mode=responses"
---
# Šema argumenata (argument schema)

## Definicija
Šema argumenata je formalni opis argumenata [[Alat|alata]] koji za svaki argument propisuje naziv, tip i dozvoljene vrednosti i navodi koji su argumenti obavezni.

## Primer
Alat zalihe u ERP-u pogona Orion ima šemu sa dva obavezna argumenta: masina, tipa string, sa obrascem „CNC-NN”, i deo, tipa string, sa dozvoljenim vrednostima vreteno i ležaj. Tehničar u poruci pominje „mašinu sedam”. Model pre [[Poziv alata|poziva]] čita šemu i šalje masina: „CNC-07”, a ne „CNC7” ili „07”, jer šema propisuje oblik. Šema pritom ne kaže da li mašina CNC-07 postoji; to se proverava u registru mašina.

## Napomene
Svaki alat ima sopstvenu šemu; zajednički je samo format zapisa, najčešće JSON Schema. U API-ju OpenAI-ja šema se navodi u polju parameters opisa funkcije, a kod Claude-a u polju input_schema.

Šema omogućava sintaksnu proveru (validacija prema šemi): da li vrednost ima propisan oblik. Ne omogućava semantičku proveru (verifikacija u registru): da li vrednost označava postojeći objekat. Oznaka „CNC-99” zadovoljava obrazac CNC-NN, iako takva mašina ne postoji.
