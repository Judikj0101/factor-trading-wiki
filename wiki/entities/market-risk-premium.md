---
type: entity
tags: [factor-model, capm]
confidence: high
last_reviewed: 2026-04-14
related: [[entities/fama-french-five-factor-model]], [[entities/smb]], [[entities/hml]]
---

# Market Risk Premium ($R_M - R_F$)

## Definíció

A piaci portfólió hozama mínusz a kockázatmentes kamatláb. Az első és legrégebbi faktor — a CAPM (Sharpe 1964, Lintner 1965) egyetlen szisztematikus kockázati faktora.

$$MKT_t = R_{M,t} - R_{F,t}$$

Ahol:
- $R_M$: a piaci portfólió (tipikusan value-weighted market index) hozama
- $R_F$: a kockázatmentes ráta (tipikusan 1 hónapos US T-bill)

## Szerepe a faktor modellekben

Minden standard faktor modell tartalmazza:
- CAPM: egyetlen faktor
- FF3: Market + SMB + HML
- Carhart 4F: Market + SMB + HML + MOM
- FF5: Market + SMB + HML + RMW + CMA

A market beta ($b_i$) a részvény piaci kockázatnak való kitettségét méri.

## Értelmezés

- $b_i > 1$: a részvény a piacnál volatilisebb (agresszívebb)
- $b_i < 1$: a részvény a piacnál kevésbé volatilis (defenzívebb)
- $b_i = 0$: piaci kockázattól független (ritka)

## Források

- [[source_summaries/fama-french-2014]]
