---
type: entity
tags: [factor-model, cross-section, investment]
confidence: high
last_reviewed: 2026-04-14
related: [[entities/fama-french-five-factor-model]], [[entities/rmw]], [[entities/hml]], [[open_questions/hml-redundancy]]
---

# CMA (Conservative Minus Aggressive)

## Definíció

Investment faktor az FF5 modellben. A konzervatívan beruházó (low investment) cégek hozamkülönbsége az agresszívan beruházókhoz képest.

$$CMA_t = R_{conservative,t} - R_{aggressive,t}$$

## Investment mérőszám

$$Inv = \frac{\Delta \text{Total Assets}}{\text{Total Assets}}$$

Azaz az eszközállomány éves növekedési üteme.

## Konstrukció (FF 2014)

- NYSE breakpoints: 30. és 70. percentilis Inv alapján
- 2×3 (size × Inv) sort
- Conservative = alacsony asset growth, Aggressive = magas asset growth

## Értelmezés

- Alacsonyabb beruházás → magasabb hozam: a konzervatívan beruházó cégek felülteljesítenek
- A DDM keretben: adott áron és profiton, a magasabb várható beruházás alacsonyabb elvárt hozamot implikál (mert a beruházás csökkenti a szabad cash flow-t)
- Kapcsolódik az "asset growth anomaly"-hoz (Cooper, Gulen & Schill 2008)

## Kapcsolat más faktorokkal

- A CMA és [[entities/rmw|RMW]] együtt képes a [[entities/hml|HML]] átlagos hozamát megmagyarázni → [[open_questions/hml-redundancy]]
- Intuitívan: a value cégek jellemzően konzervatívan beruháznak és/vagy profitábilisak, ezért a HML ezeket a dimenziókat is tükrözi

## Források

- [[source_summaries/fama-french-2014]]
