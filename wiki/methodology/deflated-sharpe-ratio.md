---
type: methodology
tags: [statistics, backtesting, overfitting, performance]
confidence: high
last_reviewed: 2026-04-14
related: [[entities/sharpe-ratio]], [[concepts/multiple-testing]], [[methodology/factor-validation]], [[methodology/backtest-overfitting-detection]], [[source_summaries/bailey-lopez-de-prado-2014-dsr]]
---

# Deflated Sharpe Ratio (DSR)

## Mikor hasznaljuk

Barmilyen backteszt vagy track record ertekelesenel, ahol:
- Tobb strategiat / konfiguriaciot teszteltunk (N > 1)
- A hozamok nem normalis eloszlasuak (negativ skewness, excess kurtosis)
- El akarjuk kerulni, hogy a [[concepts/multiple-testing|multiple testing]] felfujja a [[entities/sharpe-ratio|Sharpe ratio]]-t

## Elofeltetelek

- A tesztelt strategiak szamanak ($N$) ismerete vagy becslese
- A kivalasztott strategia napi/havi hozamai (T darab)
- A hozamok skewness ($\hat{\gamma}_3$) es kurtosis ($\hat{\gamma}_4$) becslese
- A tesztelt strategiak Sharpe ratio-jainak varianciajanak becslese ($V[\{SR_n\}]$)

## Lepesek

### 1. Rejection threshold kiszamitasa

Az "elvarhatoertek-maximum" — ennyi SR-t varhatnank pusztan veletlenbol N proba utan:

$$\hat{SR}_0 \approx \sqrt{V[\{SR_n\}]} \cdot \left((1-\gamma) \cdot Z^{-1}\left[1 - \frac{1}{N}\right] + \gamma \cdot Z^{-1}\left[1 - \frac{1}{N} \cdot e^{-1}\right]\right)$$

Ahol $\gamma \approx 0.5772$ (Euler-Mascheroni konstans).

**Intuicio:** minel tobb probat futtatunk (N no), annal magasabb $\hat{SR}_0$ → annal nehezebb "atmenni a teszten".

### 2. DSR statisztika kiszamitasa

$$DSR = Z\left[\frac{(\hat{SR} - \hat{SR}_0)\sqrt{T-1}}{\sqrt{1 - \hat{\gamma}_3 \hat{SR} + \frac{\hat{\gamma}_4 - 1}{4}\hat{SR}^2}}\right]$$

Az eredmeny egy valoszinuseg (0 es 1 kozott): annak valoszinusege, hogy a **valos** SR meghaladja a nulat, figyelembe veve:
- A probalkozasok szamat (N)
- A hozamok nem-normalitasat ($\hat{\gamma}_3, \hat{\gamma}_4$)
- A minta meretet (T)

### 3. Ertelmezes

| DSR ertek | Ertelmezes |
|---|---|
| > 0.95 | Szignifikans 95%-os szinten — elfogadhato |
| 0.90 – 0.95 | Hatareset — tovabbi validacio szukseges |
| < 0.90 | Nem szignifikans — valoszinuleg veletlenszeru |

### 4. Osszevetes Harvey et al. (2016) t > 3.0 kuzszobbel

A ket modszer komplementer:
- **Harvey et al. (2016):** fix t-statistic kuszob, a [[concepts/factor-zoo|factor zoo]] meretebol szarmaztatva
- **DSR:** strategia-specifikus kuszob, az adott kiserlet parametereibol (N, T, skewness, kurtosis)

Mindkettot erdemes alkalmazni. Ha barmellyyik elutasit → gyanus.

## Gyakori hibak

- **N alacsonyra becslese:** a kutato "elfelejti" beleszamolni az informalis probalkozasokat → DSR tul magas
- **Evesitett SR hasznalata:** a DSR-t a **napi/havi** (nem evesitett) SR-re kell szamolni, T a megfigyelesek szama
- **Normalis eloszlas feltetelezeese:** ha $\hat{\gamma}_3 = 0, \hat{\gamma}_4 = 3$-at hasznalunk de a hozamok fat-tailed → tul optimista DSR
- **Fuggetlen probak felteteleveelse:** ha a strategiak korrelalatak, N-et csokkenteni kell (ld. Bailey & Lopez de Prado 2014, Appendix 3)

## Dontesi pontok

- Ha DSR > 0.95 es t > 3.0 → **tovabb az OOS validaciora**
- Ha DSR > 0.95 de t < 3.0 → **gyanus**, tobb adat / elmelet kell
- Ha DSR < 0.95 → **elvetni** vagy ujratervezni a strategiat

## Forrasok

- [[source_summaries/bailey-lopez-de-prado-2014-dsr]]
- [[source_summaries/harvey-liu-zhu-2016]]
