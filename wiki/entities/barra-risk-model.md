---
type: entity
tags: [risk-management, factor-model, regression, portfolio]
confidence: high
last_reviewed: 2026-04-14
related: [[entities/fama-french-five-factor-model]], [[concepts/covariance-matrix]], [[entities/msci-facs]], [[source_summaries/barra-risk-model-handbook]], [[source_summaries/barra-use4-2011]]
---

# Barra Risk Model

## Definíció

A Barra (ma MSCI) által fejlesztett fundamentális multi-factor kockázati modell sorozat. Az ipari standard portfólió kockázat mérésére és dekompozíciójára intézményi befektetők számára.

## Modell matematika

A Barra MFM keretben egy részvény hozama:

$$r_i = \sum_{k=1}^{K} X_{ik} f_k + u_i$$

Ahol:
- $X_{ik}$: az $i$. részvény exposure-ja a $k$. faktorhoz
- $f_k$: a $k$. faktor hozama (cross-sectional regresszióból becsülve)
- $u_i$: specific return (részvényspecifikus, nem faktorok által magyarázott)

A portfólió variancia:

$$\sigma_p^2 = \mathbf{x}_p' \mathbf{F} \mathbf{x}_p + \mathbf{w}' \mathbf{\Delta} \mathbf{w}$$

Ahol $\mathbf{F}$ a faktor kovariancia mátrix, $\mathbf{\Delta}$ a specific risk mátrix (diagonális).

## Modell generációk (US Equity)

| Modell | Év | Fő újítás |
|---|---|---|
| USE1 | 1975 | Első multi-factor risk model |
| USE2 | 1985 | Továbbfejlesztett faktorok |
| USE3 | 1997 | Modernizált, 2002-ben napi frissítéssel bővítve |
| USE4 | 2011 | Eigenfactor adj., Regime adj., Bayesian shrinkage |

## Globális modellek

- GEM (1989) → GEM2 (2008) → GEMLT
- BIM (Barra Integrated Model): lokális + globális modellek konzisztens kombinációja

## Barra vs Fama-French

| | Barra | Fama-French |
|---|---|---|
| **Cél** | Kockázat előrejelzés | Asset pricing tesztelés |
| **Faktor hozam** | Cross-sectional WLS regresszió | Long-short portfólió sort |
| **Faktorok száma** | ~60+ | 3–5 |
| **Frissítés** | Napi | Havi |
| **Elérhetőség** | Fizetős (MSCI) | Publikus (Ken French website) |

## Limitációk

- Proprietáris — a részletes kód és adatok nem publikusak
- Drága licensz
- A modell "black box" jellege miatt nehéz validálni

## Források

- [[source_summaries/barra-risk-model-handbook]]
- [[source_summaries/barra-use4-2011]]
