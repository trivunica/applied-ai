---
tip: pojam
aliases: [structured output, strukturiran izlaz, JSON izlaz]
izvor: "Anthropic. Structured outputs, Claude Platform Docs. https://platform.claude.com/docs/en/build-with-claude/structured-outputs"
---
# Strukturisan izlaz (structured output)

## Definicija
Strukturisan izlaz je odgovor [[Jezički model|jezičkog modela]] u mašinski čitljivom formatu, najčešće JSON, koji odgovara unapred zadatoj šemi.

## Primer
Tehničar u pogonu Orion napiše: „Trebalo bi pogledati zalihe za mašinu sedam, verovatno vreteno.” Model ne vraća rečenicu istog sadržaja, već JSON {"masina": "CNC-07", "deo": "vreteno"} prema šemi alata zalihe. Program ga čita bez tumačenja. Da je kvar zapravo na ležaju, JSON bi i dalje odgovarao šemi: strukturisan izlaz garantuje oblik odgovora, a ne tačnost sadržaja.

## Napomene
Svaki [[Poziv alata|poziv alata]] je strukturisan izlaz čija je šema [[Šema argumenata|šema argumenata]] tog alata. Dokumentacija za Claude razlikuje JSON izlaz, koji ograničava format samog odgovora, i strogo pozivanje alata (strict tool use), koje garantuje da argumenti poziva odgovaraju šemi. Kod OpenAI-ja isti efekat za pozive funkcija daje strict: true u opisu funkcije.
