---
type: source_summary
tags: [factor-model, statistics, cross-section, overfitting]
confidence: high
last_reviewed: 2026-04-14
related: [[concepts/factor-zoo]], [[concepts/multiple-testing]], [[entities/fama-french-five-factor-model]], [[methodology/factor-validation]]
---

# Harvey, Liu & Zhu (2016) — ...and the Cross-Section of Expected Returns

**Szerzők:** Campbell R. Harvey, Yan Liu, Heqing Zhu
**Megjelenés:** 2016, Review of Financial Studies, v29 n1
**Raw forrás:** `raw/papers/P118_and_the_cross.md`

## Fő állítások

1. **316 faktort** katalogizáltak 313 publikált cikkből (1967–2014).
2. A szokásos t > 2.0 küszöb **nem elégséges** ha több száz faktort tesztelünk → multiple testing probléma.
3. Új faktorok számára a helyes küszöb **t > 3.0** (és növekszik az idő múlásával ahogy több faktort tesztelnek).
4. **"Most claimed research findings in financial economics are likely false."**
5. Out-of-sample validáció a legtisztább módszer, de a real-time alkalmazáshoz multiple testing framework kell.

## Faktor taxonómia

A szerzők kétszintű osztályozást adnak:

| Fő kategória | Alkategória | Példa | Db |
|---|---|---|---|
| **Common** (szisztematikus) | Financial | Market returns, squared market | 46 |
| | Macro | Consumption growth, investment | 40 |
| | Microstructure | Liquidity, trading volume | 11 |
| | Behavioral | Investor sentiment | 3 |
| | Accounting | Size, B/M | 8 |
| | Other | Momentum | 5 |
| **Characteristics** (egyedi) | Financial | Idiosyncratic volatility | 61 |
| | Microstructure | Short sale restrictions | 28 |
| | Behavioral | Analyst dispersion | 3 |
| | Accounting | PE ratio, debt/equity | 87 |
| | Other | Political contributions | 24 |

**Összesen:** 113 common + 202 characteristics = ~316 faktor

## Statisztikai keretrendszer

### Family-Wise Error Rate (FWER)
$$FWER = Pr(N_{0|r} \geq 1)$$
Legalább egy hamis felfedezés valószínűsége. Nagyon konzervatív (Bonferroni).

### False Discovery Rate (FDR)
$$FDR = E\left[\frac{N_{0|r}}{R}\right]$$
A hamis felfedezések várható aránya az összes felfedezéshez képest. Kevésbé szigorú.

A szerzők azt mutatják, hogy a t > 2.0 küszöb mellett az FWER ~100% és az FDR ~26%.

## Limitációk

- A 316 faktor alulreprezentálja a valós számot (publication bias, hidden tests).
- Elméleti alapon motivált faktoroknak alacsonyabb küszöb megengedhető.
- Kondicionális (rezsimfüggő) faktorok nem kapnak elég figyelmet az unconditional keretben.

## Kapcsolódás a rendszerhez

Ez a paper definiálja a **minőségi küszöböt** bármilyen új faktor vagy signal elfogadásához. Az MMCP-ben használt signalok validációjánál is releváns: minden signal-nek t > 3.0 felett kellene teljesítenie.
