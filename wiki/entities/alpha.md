---
type: entity
tags: [factor-model, cross-section, performance]
confidence: high
last_reviewed: 2026-04-14
related: [[entities/fama-french-five-factor-model]], [[entities/carhart-four-factor-model]], [[entities/capm]], [[entities/sharpe-ratio]], [[entities/beta]]
---

# Alpha (Jensen's Alpha)

## Definíció

A faktor regresszió interceptje ($\alpha_i$) — az a hozam amit a faktor exposure-k nem magyaráznak. Ha $\alpha > 0$: a portfólió/stratégia valódi hozzáadott értéket termel a faktor prémiumokon felül.

$$R_{it} - R_{Ft} = \alpha_i + \sum_k \beta_{ik} f_{kt} + e_{it}$$

Az $\alpha_i$ a "skill" mérőszáma: amit a menedzser a faktor tilteken felül produkál.

## Alpha különböző modellekben

| Modell | Alpha jelentése |
|---|---|
| CAPM | Hozam a piaci kockázat felett (Jensen 1968) |
| FF3 | Hozam a market + size + value faktorok felett |
| Carhart 4F | Hozam a market + size + value + momentum felett |
| FF5 | Hozam az 5 faktor felett |

**Fontos:** az alpha modell-függő. Egy stratégia ami CAPM-ben alphát mutat, FF5-ben lehet nulla (mert a "skill" valójában faktor exposure volt).

## Alpha vs faktor prémium

- **Alpha:** a faktorok által nem magyarázott részhozam — "valódi skill" vagy ismeretlen faktor
- **Faktor prémium:** szisztematikus, harvesztálható kockázati kompenzáció
- A factor investing lényege: amit korábban alpha-nak hittek, nagy része harvesztálható faktor prémium (Fama & French 2010, Kruger 2007)

## Statisztikai értékelés

- Alpha szignifikanciája: t-statistic az $\alpha_i$-ra
- GRS teszt: az összes alpha együttes szignifikanciájának tesztje
- Harvey et al. (2016) figyelmeztetése: t > 3.0 küszöb szükséges → [[concepts/multiple-testing]]

## Források

- [[source_summaries/fama-french-2014]]
- [[source_summaries/kruger-2007]]
