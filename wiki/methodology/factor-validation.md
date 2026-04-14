---
type: methodology
tags: [statistics, factor-model, backtesting]
confidence: medium
last_reviewed: 2026-04-14
related: [[concepts/factor-zoo]], [[concepts/multiple-testing]], [[source_summaries/harvey-liu-zhu-2016]]
---

# Factor Validation — Faktor validációs eljárás

## Mikor használjuk

Bármilyen új faktor, signal, vagy anomália értékelésénél mielőtt portfólióba építenénk.

## Előfeltételek

- Egyértelmű faktor definíció (milyen változó, milyen sort, milyen portfólió)
- Elegendő historikus adat (min. 10+ év havi adatoknál)
- Tisztában lenni a korábbi tesztek számával (multiple testing kontextus)

## Lépések

### 1. Statisztikai szignifikancia
- t-statistic kiszámítása a faktor prémiumra
- **Küszöb:** t > 3.0 (Harvey et al. 2016)
- Ha t < 2.0: elvetni
- Ha 2.0 < t < 3.0: csak erős elméleti motivációval fogadható el

### 2. Elméleti motiváció
- Van-e közgazdasági elmélet ami a prémiumot magyarázza?
- Kockázati kompenzáció vs behavioral bias vs institutional friction?
- Elméleti alappal rendelkező faktoroknak enyhébb küszöb, de t > 2.0 minimum

### 3. Out-of-sample validáció
- Más időszak (pl. pre-sample, post-sample)
- Más piac/régió (US → Európa → KKE → EM)
- Más asset class (equity → bonds → commodities)

### 4. Robusztusság
- Érzékenység a faktor definíció módosítására (breakpoints, rebalance frekvencia)
- Érzékenység a minta választásra (subperiod analysis)
- Tranzakciós költségek figyelembevétele

### 5. Közgazdasági magnitúdó
- Mekkora az éves prémium?
- Reális-e a megvalósítás (turnover, kapacitás, likviditás)?
- Túléli-e a tranzakciós költségeket?

## Gyakori hibák

- **Data snooping:** sok változatot próbálni és csak az "egyiket" publikálni
- **Look-ahead bias:** jövőbeli információ használata a faktor konstrukcióban
- **Survivorship bias:** csak túlélő cégek bevonása
- **Microcap dominancia:** az eredmény a legkisebb, legkevésbé kereskedhető részvényekből jön

## Döntési pontok

- Ha t < 3.0 és nincs elméleti alap → **elvetni**
- Ha t > 3.0 de nincs OOS validáció → **tovább tesztelni** más mintán
- Ha t > 3.0, van elméleti alap, és OOS is működik → **elfogadni**, portfólióba építeni

### 6. Backtest overfitting ellenorzes
- [[methodology/deflated-sharpe-ratio|Deflated Sharpe Ratio (DSR)]]: DSR > 0.95 szukseges
- [[methodology/backtest-overfitting-detection|PBO (CSCV)]]: PBO < 0.50 szukseges
- Minimum Backtest Length (MinBTL) ellenorzes

## Források

- [[source_summaries/harvey-liu-zhu-2016]]
- [[source_summaries/bailey-lopez-de-prado-2014-dsr]]
- [[source_summaries/bailey-borwein-lopez-de-prado-zhu-2015-pbo]]
- [[source_summaries/simonian-2024-model-validation]]
