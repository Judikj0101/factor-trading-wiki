---
type: concept
tags: [risk-management, statistics, portfolio]
confidence: high
last_reviewed: 2026-04-14
related: [[entities/barra-risk-model]], [[source_summaries/barra-risk-model-handbook]], [[source_summaries/barra-use4-2011]]
---

# Kovariancia mátrix (Covariance Matrix)

## Mi ez

A kovariancia mátrix ($\mathbf{\Sigma}$) tartalmazza az összes részvénypár közötti kovarianciát. Ez a portfólió kockázat számítás alapja (Markowitz 1952). A portfólió variancia:

$$\sigma_p^2 = \mathbf{w}' \mathbf{\Sigma} \mathbf{w}$$

## Miért fontos

- A Markowitz-féle portfólió optimalizálás központi inputja
- $N$ részvénynél $N(N+1)/2$ paramétert kell becsülni → hatalmas, zajossá válik
- A Barra multi-factor megközelítés megoldása: struktúrált kovariancia mátrix

## A Barra megoldás

Ahelyett, hogy közvetlenül becsülnénk a teljes $N \times N$ kovariancia mátrixot, a Barra modell szétbontja:

$$\mathbf{\Sigma} = \mathbf{X} \mathbf{F} \mathbf{X}' + \mathbf{\Delta}$$

Ahol:
- $\mathbf{X}$: exposure mátrix ($N \times K$)
- $\mathbf{F}$: faktor kovariancia mátrix ($K \times K$, $K \ll N$)
- $\mathbf{\Delta}$: specific risk mátrix (diagonális, $N \times N$)

Mivel $K \approx 60 \ll N \approx 3000$, a becslési probléma drasztikusan egyszerűsödik.

## USE4 fejlesztések

- **Eigenfactor Risk Adjustment:** csökkenti a sampling error hatását az optimalizált portfóliók kockázat-előrejelzésében
- **Volatility Regime Adjustment:** az aktuális piaci volatilitási szinthez kalibrálja az előrejelzést
- **Exponenciális súlyozás:** frissebb adatok nagyobb súlyt kapnak

## Érintett entitások

- [[entities/barra-risk-model]]

## Források

- [[source_summaries/barra-risk-model-handbook]]
- [[source_summaries/barra-use4-2011]]
