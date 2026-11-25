---
tip: pojam
aliases: [tool result, tool_result, function_call_output]
izvor: "Anthropic. Handle tool calls, Claude Platform Docs. https://platform.claude.com/docs/en/agents-and-tools/tool-use/handle-tool-calls"
---
# Rezultat alata (tool result)

## Definicija
Rezultat alata je podatak koji [[Okruženje agenta|okruženje agenta]] vraća [[Jezički model|jezičkom modelu]] posle izvršenja [[Poziv alata|poziva alata]], bez obzira na to da li je izvršenje uspelo.

## Primer
Model u pogonu Orion traži poziv alata zalihe za CNC-07 i vreteno. ERP u tom trenutku ne odgovara, pa okruženje agenta vraća modelu poruku „ERP nije dostupan, pokušaj ponovo za 5 minuta”. I ta poruka je rezultat alata: model je čita kao i uspešan odgovor i na osnovu nje bira sledeći korak, umesto da zaključi da vretena nema na stanju.

## Napomene
Kod Claude-a rezultat se vraća kao blok tool_result, vezan za poziv preko polja tool_use_id, a neuspeh se može označiti poljem is_error. Kod OpenAI-ja rezultat se vraća kao stavka function_call_output, vezana za poziv preko polja call_id.

Razlikuju se tri oblika: uspešan rezultat, poruka o grešci i prazan rezultat. Prazan rezultat se najlakše pogrešno tumači, jer model iz odsustva podataka može da izvede zaključak koji podaci ne podržavaju (halucinacija).
