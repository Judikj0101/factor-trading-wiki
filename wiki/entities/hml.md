---
type: entity
tags: [factor-model, cross-section, value]
confidence: high
last_reviewed: 2026-04-14
related: [[entities/fama-french-five-factor-model]], [[entities/smb]], [[entities/rmw]], [[entities/cma]], [[concepts/value-premium]], [[open_questions/hml-redundancy]]
---

# HML (High Minus Low)

## Definíció

Value faktor a Fama-French modellekben. A magas book-to-market (B/M) részvények hozamkülönbsége az alacsony B/M részvényekhez képest.

$$HML_t = R_{high\;B/M,t} - R_{low\;B/M,t}$$

## Konstrukció

### FF3 (1993) — eredeti definíció
- NYSE breakpoints: 30. és 70. percentilis B/M alapján
- 2×3 independent sort: Size × B/M
- $HML = \frac{1}{2}(SH + BH) - \frac{1}{2}(SL + BL)$

### FF5 (2014) — azonos konstrukció
- 2×3 (size × B/M) sortból: HML = avg(Small Value, Big Value) − avg(Small Growth, Big Growth)

## Értelmezés

- Pozitív HML exposure: a portfólió value részvényekhez hasonlóan viselkedik
- A [[concepts/value-premium]] az egyik legrégebb óta dokumentált anomália
- Magas B/M → a piac alacsonyra értékeli → vagy nagyobb kockázat, vagy mispricing

## HML redundancia az FF5-ben

Fama & French (2014) meglepő eredménye: ha RMW és CMA benne van a modellben, a HML átlagos hozamát a többi faktornak való kitettség teljesen magyarázza. Ez azt jelenti, hogy a HML információtartalma benne van a profitability és investment faktorokban.

**Figyelem:** a szerzők maguk jelzik, hogy ez az eredmény mintaspecifikus lehet (US 1963–2013).

Részletek: [[open_questions/hml-redundancy]]

## Források

- [[source_summaries/fama-french-1993]]
- [[source_summaries/fama-french-2014]]
