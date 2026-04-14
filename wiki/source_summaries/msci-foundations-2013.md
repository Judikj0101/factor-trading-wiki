---
type: source_summary
tags: [factor-model, factor-investing, risk-premia]
confidence: high
last_reviewed: 2026-04-14
related: [[entities/fama-french-five-factor-model]], [[entities/smb]], [[entities/hml]], [[entities/momentum]], [[entities/low-volatility]], [[entities/quality-factor]], [[entities/dividend-yield-factor]], [[concepts/factor-zoo]], [[concepts/factor-cyclicality]]
---

# MSCI (2013) — Foundations of Factor Investing

**Szerzők:** Jennifer Bender, Remy Briand, Dimitris Melas, Raman Aylur Subramanian
**Megjelenés:** December 2013, MSCI Research Insight
**Raw forrás:** `raw/papers/Foundations_of_Factor_Investing.md`

## Fő állítások

1. **Hat kockázati prémium faktort** azonosítanak: Value, Low Size, Low Volatility, High Yield, Quality, Momentum.
2. Megkülönböztetnek **generic faktorokat** (risk-et magyaráznak de nem termelnek prémiumot, pl. Growth, Liquidity) és **risk premia faktorokat** (tartós prémium + szisztematikus kockázat).
3. Aktív menedzserek hozamainak ~50%-a faktor tiltekre vezethető vissza (Mok, Bender, Hammond 2013).
4. A faktor hozamok **erősen ciklikusak** — mindegyik faktor tartósan alulteljesíthet.
5. A ciklikusság oka lehet, hogy a prémiumokat nem arbitrálják el.
6. **Faktor diverzifikáció** csökkenti az alulteljesítés periódusait.

## Hat risk premia faktor

| Faktor | Mérőszám | Prémium oka (risk-based) | Prémium oka (behavioral) |
|--------|----------|--------------------------|--------------------------|
| Value | B/P, E/P, CF/P | Magasabb üzleti ciklus kockázat | Loss aversion, errors-in-expectations |
| Low Size | Market cap | Likviditási, distress kockázat | Errors-in-expectations |
| Momentum | 3-12 havi relatív hozam | Tail risk, üzleti ciklus | Underreaction, overreaction, herding |
| Low Volatility | Std dev, beta | N/A | Lottery effect, overconfidence, leverage aversion |
| Dividend Yield | Dividend yield | Üzleti ciklus kockázat | Errors-in-expectations |
| Quality | ROE, earnings stability, leverage | N/A | Errors-in-expectations |

## Faktor tipológia

Három kategória a modellezésben:
1. **Makroökonómiai faktorok** — GDP, infláció, yield curve meglepetések
2. **Statisztikai faktorok** — PCA alapú, előre nem specifikált
3. **Fundamentális faktorok** — stock characteristics (a leggyakoribb ma)

Két módszer a faktor hozam becslésére:
- **Fama-French módszer:** portfólió sortolás (long-short)
- **Barra módszer:** cross-sectional regresszió

## Limitációk

- MSCI saját termékei (Factor Indexes) promotálása — nem teljesen semleges forrás
- A 2013 utáni periódust nem tartalmazza (value underperformance, growth dominancia)

## Kapcsolódás a rendszerhez

Jó áttekintés a factor investing koncepcionális alapjairól. A ciklikusság és a faktor diverzifikáció a portfólió construction szempontjából kulcsfontosságú.
