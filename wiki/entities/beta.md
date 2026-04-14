---
type: entity
tags: [factor-model, capm, risk-management]
confidence: high
last_reviewed: 2026-04-14
related: [[entities/capm]], [[entities/market-risk-premium]], [[entities/alpha]], [[entities/low-volatility]]
---

# Beta (piaci béta)

## Definíció

Egy részvény vagy portfólió szisztematikus kockázata — a piaci hozam változásaira való érzékenysége.

$$\beta_i = \frac{Cov(R_i, R_M)}{Var(R_M)}$$

## Értelmezés

| Beta érték | Jelentés |
|---|---|
| $\beta = 1$ | A piacnak megfelelő kockázat |
| $\beta > 1$ | Agresszívebb, mint a piac (ciklikus, tech, small cap) |
| $\beta < 1$ | Defenzívebb, mint a piac (utilities, staples, health) |
| $\beta = 0$ | Piaci kockázattól független (ritka) |
| $\beta < 0$ | Inverz piaci mozgás (pl. short pozíció, egyes hedge stratégiák) |

## CAPM keretben

A CAPM szerint a béta az **egyetlen** releváns kockázati mérőszám: magasabb béta → magasabb elvárt hozam. De empirikusan ez **nem teljesül** jól — lásd [[entities/low-volatility|Low Volatility anomália]].

## Multi-factor keretben

Az FF5-ben a piaci béta ($b_i$) csak az egyik exposure — a size, value, profitability és investment bétái is számítanak. A "béta" szó ilyenkor bármely faktornak való kitettséget jelölheti:

$$R_{it} - R_{Ft} = \alpha_i + \underbrace{b_i}_{market\;\beta}(R_{Mt} - R_{Ft}) + \underbrace{s_i}_{size\;\beta} SMB_t + \underbrace{h_i}_{value\;\beta} HML_t + \ldots$$

## Becslési kérdések

- **Becslési ablak:** 1 év napi, 3 év heti, 5 év havi — az eredmény érzékeny
- **Barra modell:** a bétát a cross-sectional regresszióból és a faktor kovariancia mátrixból számítja, nem egyszerű historikus regresszióból
- **Shrinkage:** a szélsőséges béta becsléseket a piac felé húzzák (Vasicek 1973)

## Források

- [[source_summaries/barra-risk-model-handbook]]
- [[source_summaries/msci-foundations-2013]]
