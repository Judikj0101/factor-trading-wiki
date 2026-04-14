---
type: source_summary
tags: [risk-management, factor-model, regression, covariance]
confidence: high
last_reviewed: 2026-04-14
related: [[entities/barra-risk-model]], [[concepts/covariance-matrix]]
---

# Barra USE4 Methodology Notes (2011)

**Szerzők:** Jose Menchero, D.J. Orr, Jun Wang
**Megjelenés:** August 2011, MSCI Model Insight
**Raw forrás:** `raw/standards/USE4_Methodology_Notes_August_2011.md`

## Fő tartalom

A Barra US Equity Model negyedik generációjának (USE4) technikai dokumentációja.

## Fő innovációk a USE3-hoz képest

1. **Eigenfactor Risk Adjustment** — sampling error csökkentése a kovariancia mátrixban → jobb kockázat-előrejelzés optimalizált portfóliókra
2. **Volatility Regime Adjustment** — a faktor volatilitások és specific risk kalibrálása az aktuális piaci szinthez
3. **Country factor** — tiszta industry hatás szétválasztása a piaci hatástól
4. **Napi specific risk modell** — daily asset-level specific returns alapján
5. **Bayesian shrinkage** — specific risk bias csökkentése
6. **Multiple industry exposures** — GICS alapú
7. **Short-term (USE4S) és long-term (USE4L) verziók** — eltérő prediction horizon

## Modell struktúra

- **Style faktorok:** ~10 risk index (Volatility, Momentum, Size, Value, Growth, stb.)
- **Industry faktorok:** ~50+ GICS alapú
- **Country factor:** 1 (US market)
- **Faktor hozam becslés:** weighted cross-sectional regression (WLS)
- **Kovariancia mátrix:** exponenciális weighting + Eigenfactor adjustment + Regime adjustment

## Elméleti kontextus

A USE4 a Markowitz (1952) → Tobin (1958) → Sharpe/CAPM (1964) → Rosenberg/Barra (1974) vonal legújabb iterációja. A cél: a kovariancia mátrix minél pontosabb becslése portfólió optimalizáláshoz.

## Kapcsolódás a rendszerhez

A USE4 a gyakorlatban használt kockázati modell. Ha portfólió optimalizálást vagy risk attribution-t végzünk, a Barra faktorok az ipari standard.
