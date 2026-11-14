---
tip: pojam
aliases: [tool, funkcija, function]
izvor: "OpenAI. Function calling, odeljak How it works. https://developers.openai.com/api/docs/guides/function-calling?api-mode=responses"
---
# Alat (tool)

## Definicija
Alat je imenovana operacija spoljnog sistema koju [[Jezički model|jezički model]] može da zatraži navođenjem imena i vrednosti argumenata, a koju izvršava program izvan modela.

## Primer
Tehničar održavanja pita asistenta u pogonu Orion: „Da li imamo rezervno vreteno za CNC-07?” Asistent ima na raspolaganju alat zalihe, koji čita stanje delova u ERP-u. Model ne pristupa ERP-u. Umesto odgovora traži izvršenje alata zalihe sa argumentima masina: „CNC-07” i deo: „vreteno”. [[Okruženje agenta|Okruženje agenta]] izvršava upit u ERP-u i vraća modelu „na_stanju: 1”, a model na osnovu toga odgovara da je jedno vreteno na stanju. Model je izabrao alat i argumente, ali upit u ERP-u nije izvršio on.

## Napomene
U dokumentaciji OpenAI-ja koriste se nazivi alat (tool) i funkcija (function): funkcija je vrsta alata čiji su argumenti opisani JSON šemom (videti [[Šema argumenata]]).

Alat nije sam spoljni sistem, već jedna imenovana operacija nad njim. ERP nije alat; zalihe, rezervacije i zakazi_servis su tri alata koje ERP izlaže.
