---
type: entity
tags: [factor-model, cross-section, profitability]
confidence: high
last_reviewed: 2026-04-14
related: [[entities/fama-french-five-factor-model]], [[entities/cma]], [[entities/hml]], [[open_questions/hml-redundancy]]
---

# RMW (Robust Minus Weak)

## Definíció

Profitability faktor az FF5 modellben. A magas operatív profitabilitású (robust) cégek hozamkülönbsége az alacsony profitabilitásúakhoz (weak) képest.

$$RMW_t = R_{robust,t} - R_{weak,t}$$

## Operatív profitabilitás (OP) definíció

$$OP = \frac{\text{Revenue} - \text{COGS} - \text{SGA} - \text{Interest Expense}}{\text{Book Equity}}$$

(Novy-Marx 2013 gross profitability változata is releváns: Revenue − COGS / Total Assets)

## Konstrukció (FF 2014)

- NYSE breakpoints: 30. és 70. percentilis OP alapján
- 2×3 (size × OP) sort
- Hasonló struktúra mint az SMB és HML

## Értelmezés

- Profitábilisabb cégek magasabb hozamot termelnek — ez ellentmond a naiv "magas profit = alacsony kockázat" logikának
- A DDM keretben: adott áron a magasabb várható profit magasabb elvárt hozamot implikál
- Az RMW és [[entities/cma|CMA]] együttesen képesek a [[entities/hml|HML]] információtartalmát helyettesíteni

## Kapcsolódó kutatás

- Novy-Marx (2013): gross profitability premium — az RMW előfutára
- A profitability faktor robusztusabb, mint a size prémium

## Források

- [[source_summaries/fama-french-2014]]
