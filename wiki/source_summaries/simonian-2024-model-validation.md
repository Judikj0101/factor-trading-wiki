---
type: source_summary
tags: [backtesting, cross-validation, risk-management, performance, statistics]
confidence: high
last_reviewed: 2026-04-14
related: [[entities/sharpe-ratio]], [[methodology/factor-validation]], [[methodology/backtesting]], [[methodology/cross-validation]], [[methodology/stress-testing]], [[concepts/multiple-testing]]
---

# Simonian (2024) — Investment Model Validation: A Guide for Practitioners

**Szerzo:** Joseph Simonian
**Kiado:** CFA Institute Research Foundation (monograph)
**Raw forras:** `raw/standards/investment-model-validation.md`

## Attekintes

Atfogo gyakorlati utmutato befektetesi modellek validalasahoz. A fo uuzenet: a model validacio nem csak backtesztelest jelent — sokkal szelesebb korut, a falsification elvet kell kovetni (mint a termeszettudomanyokban).

## Fo fejezetek es tanulsagok

### 1. Validacios filozofia
- A penzugy **adatszegeny** a termeszettudomanyokhoz kepest: egy S&P 500 tortenet van, nem szazak
- A standard megkozelltes ("eureka" backteszt) **data snooping**-hoz vezet
- Helyes megkozelltes: **falsification** (Popper) — probaljuk megcafolni a modellt, ne megerositeni
- **Prophylaxis** (sakk analogia, Nimzowitsch/Petrosian): minden lepes egyben vedekezes is — a modell fejlesztesnel gondoljunk az ellenervekre

### 2. Backtesting
- **In-sample vs out-of-sample:** az IS tesztek "csalas" — nem adnak informaciot a modell generalizalhatosagarol
- **Building blocks:** signal(ok), entry/exit szabalyok, poziciomeretezes, rebalancing
- **Buktatuk:**
  - **Overfitting:** alacsony bias, magas variancia — a modell a zajt tanulja meg
  - **Inception point risk:** mas kezdopont → mas eredmeny (selection bias)
  - **Survivorship bias:** csak tulelok → felfelekre torzitas
  - **Look-ahead bias:** a kutato tudat alatt felhasznalhja a jovobeli ismereteit
  - **Data snooping:** sok modellvaltozat → a legjobb megtalalas garantalt

### 3. Cross-validation
- **Holdout:** egyszerű de magas varianciaju, nem megbizhato
- **K-fold:** stabilabb, k-szor ismetli a felosztast
- **LOOCV:** torzitatlan de szamitasigenyes
- **Idosoros CV:**
  - **Rolling window:** fix meretu ablak mozog elore
  - **Expanding window:** az ablak no
  - **Block time-series CV:** memoriahatast kikuszobolheto blokkolassal a foldok kozott
- **Regime-switching modellek** (Hamilton 1989, Filardo 1994) segithetnek a fold meretek meghatarozasaban

### 4. Performance measurement
- **Return metrikai:** simple return, cumulative, time-weighted, modified Dietz
- **Kockazati metrikai:**
  - Variancia / std deviation (volatility)
  - [[entities/sharpe-ratio]]: $SR = (r_P - r_f) / \sigma_P$
  - Skewness, kurtosis — a normalis eloszlas feltevesenek ellenorzese
  - Covariance, correlation, autocorrelation
  - Downside risk → Sortino ratio
  - VaR (parametrikus, historikus, Monte Carlo)
  - Information Ratio: $IR = \overline{ER} / \hat{\sigma}_{ER}$
  - Treynor ratio: $(r_P - r_f) / \beta_P$
  - Fama decomposition

### 5. Szintetikus adatok
- **Monte Carlo szimulacio**
- **Bootstrap**
- **Generative Adversarial Networks (GAN)** — uj megkozellites szintetikus idosor generalasra

### 6. Modell-osszehasonlitas
- Akaike Information Criterion (AIC), Schwarz (BIC)
- McNemar teszt
- Prediktiv pontossag meresek

### 7. Stress testing es scenario analysis
- Stress testing: extrém piaci korulmenyek tesztelese
- Reverse stress testing: milyen korulmenyek kozott omlik ossze a modell?
- Scenario analysis: specifikus scenariok (pl. kamatemeles, recesszio)

### 8. Kozgazdasagi elmeleti osszhangarossag
- A modellnek osszhangrban kell lennie a befektetesi elmelettel
- Ha a modell a teoriaval ellentetes eredmenyt ad → gyanus, fokozott vizsgalat

## Kulcs idezetek

> "It is remarkable how decidedly *unscientific* investment strategy development and model validation often are."

> "Most investment and trading strategies developed in this manner will be 'false positive' strategies."

## Limitaciok

- Attekintes jellegű (nem ad uj eredmenyt, hanem szintetizalja a meglevot)
- Nem tartalmaz konkret kodot vagy algoritmust
- Nem tárgyalja reszletesen a multiple testing korrekciokat (Bailey/Lopez de Prado munkaira hivatkozik de nem melyiti el)

## Kapcsolodas a rendszerhez

Ez a monograph a [[methodology/backtesting]] es [[methodology/cross-validation]] meglapozasa. A CFA Institute "pecsetje" raadja az ipari standard jelleget. A falsification elv osszhangban van a [[methodology/factor-validation]] szigoru megkozelitesevel (t > 3.0). A stress testing/scenario analysis modszerek kiegeszitik a statisztikai validaciot a [[concepts/multiple-testing]] kezelesen tul.
