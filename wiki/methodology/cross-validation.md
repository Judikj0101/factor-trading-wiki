---
type: methodology
tags: [cross-validation, backtesting, statistics, time-series]
confidence: high
last_reviewed: 2026-04-14
related: [[methodology/backtesting]], [[methodology/backtest-overfitting-detection]], [[methodology/factor-validation]], [[source_summaries/simonian-2024-model-validation]], [[source_summaries/bailey-borwein-lopez-de-prado-zhu-2015-pbo]]
---

# Cross-Validation — Keresztvalidacio befektetesi modellekhez

## Mikor hasznaljuk

A backteszt eredmenyek robusztussaganak ellenorzesere. A cross-validation a holdout modszer altalanositasa — rendszeresen fellosztja az adatot train/validation/test reszekre, csokkentve az egyetlen split-bol eredo variaciot.

## Alapmodszerek (altalanos)

### 1. Holdout
- 70-80% train, 20-30% test
- **Elony:** egyszerű
- **Hatrany:** magas variancia, egyetlen split → kovetkezletes fugghet a valasztastol

### 2. K-fold cross-validation
- Az adat k reszre osztva, k-szor futtatva (k-1 train, 1 test)
- Az atlagos teljesitmeny stabilabb becsless
- **Hatrany:** penzugyi idosoroknal a kronologiai rendet felboriltja!

### 3. Leave-One-Out (LOOCV)
- K-fold extrem valtozata: minden egyes megfigyeles egyszer test
- Torzitatlan de szamitasigenyes
- Ritkán hasznalt penzugyi kontextusban

## Idosoros cross-validation (time-series CV)

A fenti altalanos modszerek **nem alkalmazhatok kozvetlenul** penzugyi idosorokra, mert az adatok kronologiai fuggoseggel birnak (autocorrelation). Az idosoros CV biztosivtja, hogy a train adat mindig **megelozi** a test adatot.

### Rolling window CV
- Fix meretu train ablak mozog elore az idoben
- Minden lepes: train az ablakban, test a kovetkezo periodusban
- **Elony:** friss adatot hasznlal, nem felteteleezi stacionaritast a teljes mintaban
- **Hatrany:** fix ablak → az ablak meretenek valasztasa szubjektiv

### Expanding window CV
- A train halmazz no minden lepessel (minden korabbi adat benne van)
- **Elony:** tobb adat → stabilabb becsles
- **Hatrany:** regi, irrelevans adatok is befolyasoljak a modellt

### Block time-series CV
- A foldok kozott **blokkolt (kihagyott) megfigyelessek** vannak
- A blokkok hossza ≈ az idosor memoraiajanak hossza (autoregreszsios rend)
- **Cél:** a foldok kozotti memoria-hatast kikuszobolni
- **Regime-switching modellek** (Hamilton 1989) segithetnek a fold es blokk meretek meghatarozasaban

## Specialis: CSCV (Combinatorially Symmetric Cross-Validation)

A [[source_summaries/bailey-borwein-lopez-de-prado-zhu-2015-pbo|Bailey et al. (2015)]] altal javasolt modszer kifejezetten a **backtest overfitting** meresere:

1. Idosor feloszlasa S egyenlo reszre
2. Minden lehetseges $\binom{S}{S/2}$ IS/OOS feloisztas vizsgalata
3. Az IS-optimalis strategia OOS rangjainak mereese
4. **Output: PBO** (Probability of Backtest Overfitting)

Reszletek: [[methodology/backtest-overfitting-detection]]

## Gyakorlati iranyelvek

| Szempont | Javaslat |
|---|---|
| Adat hossz | Min. 1000 megfigyeles (Weiss & Kulikowski) |
| Fold szam | 5-10 fold altalaban megfelelo |
| Blokk meret | Autocorrelation fueggveny alapjan (pl. AR rend) |
| Regime valtas | Ha van → regime-switching alapu foldok |
| Szintetikus kiegeszites | Monte Carlo / bootstrap a CV kiegeszitesere |

## Gyakori hibak

- **Idosoros adat K-fold-dal:** a kronologiai rend felborulasa → look-ahead bias
- **Tul rovid OOS:** nincs eleg statisztikai ero
- **Autocorrelacio ignoralasa:** a fold-ok kozotti memoria → hamis jo eredmenyek
- **Egyetlen CV mint "bizonyitek":** a CV egy diagnosztikai eszkoz, nem garantia

## Forrasok

- [[source_summaries/simonian-2024-model-validation]]
- [[source_summaries/bailey-borwein-lopez-de-prado-zhu-2015-pbo]]
