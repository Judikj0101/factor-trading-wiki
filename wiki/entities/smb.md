---
type: entity
tags: [factor-model, cross-section, size]
confidence: high
last_reviewed: 2026-04-14
related: [[entities/fama-french-five-factor-model]], [[entities/hml]], [[entities/rmw]], [[entities/cma]]
---

# SMB (Small Minus Big)

## Definíció

Size faktor a Fama-French modellekben. A kis piaci kapitalizációjú részvények hozamkülönbsége a nagy kapitalizációjúakhoz képest.

$$SMB_t = R_{small,t} - R_{big,t}$$

## Konstrukció

### FF3 (1993) — eredeti definíció
- NYSE median market cap alapján Size sort (Small vs Big)
- 2×3 independent sort: Size × B/M
- $SMB = \frac{1}{3}(SL + SM + SH) - \frac{1}{3}(BL + BM + BH)$

### FF5 (2014) — bővített definíció
- Az SMB három independent sort átlagából áll: B/M, OP, és Inv dimenziók mentén
- Átlagos hozam: ~0.29–0.30%/hó (US, 1963–2013)
- Standard deviáció: ~2.87–3.13%/hó

## Értelmezés

- Pozitív SMB exposure: a portfólió kisebb cégekhez hasonlóan viselkedik
- A size prémium léte vitatottabb, mint a value prémiumé — lásd [[concepts/factor-zoo]]
- A kis cégek magasabb hozamát a magasabb likviditási kockázat, információs aszimmetria és tranzakciós költségek magyarázhatják

## Limitációk

- A size prémium időben változó, egyes periódusokban eltűnik
- Erősen függ a microcap részvények bevonásától
- Institutional constraints: sok intézményi befektető nem tud microcap-ba fektetni

## Források

- [[source_summaries/fama-french-1993]]
- [[source_summaries/fama-french-2014]]
