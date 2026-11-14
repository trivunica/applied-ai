---
tip: pojam
aliases: [parallel tool calls, parallel tool use]
izvor: "Anthropic. Parallel tool use, Claude Platform Docs. https://platform.claude.com/docs/en/agents-and-tools/tool-use/parallel-tool-use"
---
# Paralelno pozivanje alata (parallel tool calls)

## Definicija
Paralelno pozivanje alata je mogućnost [[Jezički model|jezičkog modela]] da u jednom odgovoru zatraži više [[Poziv alata|poziva alata]], pre nego što vidi [[Rezultat alata|rezultat]] bilo kog od njih.

## Primer
U koraku dijagnoze za CNC-07 u pogonu Orion model u istom odgovoru traži dva poziva: ocitaj_vibracije i zalihe za vreteno. Nijedan poziv ne koristi rezultat drugog, pa [[Okruženje agenta|okruženje agenta]] izvršava oba i vraća oba rezultata zajedno. Model dolazi do dijagnoze u dva odgovora umesto u tri. Rezervaciju vretena ne traži u istom odgovoru, jer njen argument zavisi od rezultata dijagnoze.

## Napomene
Pojam se odnosi na ono što model traži, a ne na način izvršenja: okruženje može pozive izvršiti istovremeno ili redom. Kod OpenAI-ja paralelni pozivi se isključuju parametrom parallel_tool_calls postavljenim na false.

Granicu postavlja zavisan poziv, odnosno poziv čiji argumenti zavise od rezultata drugog poziva. Paralelno idu samo pozivi koji ne menjaju povezana stanja (videti [[Alat koji menja stanje]]).
