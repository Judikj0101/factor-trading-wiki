---
type: methodology
tags: [cross-section, statistics, regression, factor-model, methodology]
confidence: high
last_reviewed: 2026-04-15
related: [[entities/capm]], [[entities/beta]], [[entities/fama-french-five-factor-model]], [[source_summaries/fama-macbeth-1973]], [[source_summaries/shanken-zhou-2006]], [[source_summaries/fama-french-1992]]
---

# Fama-MacBeth Regresszió

## Mikor használjuk

Cross-sectional faktor vizsgálatnál: annak tesztelésére, hogy egy adott karakterisztika (size, B/M, momentum, stb.) szignifikánsan előrejelzi-e a jövőbeli részvényhozamokat, miközben más faktorokra kontrollálunk.

## Előfeltételek

- Legalább 5+ év havi hozamadat
- A faktorterhelések (bétabecslések) az első lépésből rendelkezésre állnak
- A karakterisztika minden periódusban frissíthető (pl. havi BE/ME frissítés)

## A kétlépéses eljárás

### 1. lépés — Idősoros bétabecslés (Time-series pass)

Minden $i$ részvényre (vagy portfólióra) idősoros OLS regresszió:

$$R_{i,t} = \alpha_i + \beta_i^{MKT} R_{M,t} + \beta_i^{SMB} SMB_t + \beta_i^{HML} HML_t + \epsilon_{i,t}$$

**Ajánlott:** Portfóliók (pl. 25 méret×B/M portfólió) alkalmazása az **EIV-probléma (errors-in-variables)** csökkentésére. Az egyedi részvény bétabecslés zajos.

### 2. lépés — Keresztmetszeti regresszió (Cross-sectional pass)

Minden $t$ időpontban cross-sectional OLS:

$$R_{i,t} = \gamma_{0,t} + \gamma_{1,t} \hat{\beta}_i^{MKT} + \gamma_{2,t} \hat{\beta}_i^{SMB} + \gamma_{3,t} \hat{\beta}_i^{HML} + \epsilon_{i,t}$$

- $\hat{\gamma}_{k,t}$: az adott hónapban becsült kockázati prémium a $k$-adik faktorra
- Minden hónapban külön regresszió → **T darab koefficiensbecslés** keletkezik

### 3. Inferencia

Az átlagos prémium és standard error:

$$\bar{\gamma}_k = \frac{1}{T} \sum_{t=1}^T \hat{\gamma}_{k,t}$$

$$SE(\bar{\gamma}_k) = \frac{SD(\hat{\gamma}_{k,t})}{\sqrt{T}}$$

**t-statisztika:**

$$t_k = \frac{\bar{\gamma}_k}{SE(\bar{\gamma}_k)}$$

A keresztmetszeti korrelációt **automatikusan kezeli** — nem kell Newey-West korrekció a megfelelő standard error számításhoz.

## Shanken-korrekció (ajánlott)

Az FM standard errorok **alulbecsülik** a valódi szórást, mert a béták mért (becsült) értékek, nem a valódi bétákat. A Shanken (1992) korrekció:

$$SE_{Shanken} = SE_{FM} \times \sqrt{1 + \hat{\lambda}^{M \top} \hat{\Sigma}_f^{-1} \hat{\lambda}^M}$$

ahol $\hat{\lambda}^M$ a Sharpe-ráta vektora és $\hat{\Sigma}_f$ a faktorhozamok kovariancia mátrixa.

## Karakterisztika vs. béta megközelítés

Két változat létezik:

| Verzió | 1. lépés | 2. lépés regressor |
|---|---|---|
| **Béta-alapú** | Bétabecsléssel | Becsült bétákat használ |
| **Karakterisztika-alapú** | Nincs | Közvetlen karakterisztikát (pl. log ME) |

A karakterisztika-alapú verzió egyszerűbb és empirikusan hasonló eredményt ad (Fama & French 1992). Az összetettebb béta-alapú verzió erősebb elméleti alap.

## Gyakori hibák

1. **EIV-probléma ignorálása:** Egyedi részvény bétákon futtatott FM alulbecsüli a prémiumot
2. **Shanken-korrekció elhagyása:** A t-statisztika felülbecslése
3. **Mikrostruktúra zaj:** Havi regressziók erősen zajos egyedi részvény hozamokon → portfóliós aggregálás javasolt
4. **Túl kevés T:** Ha T < 60 hónap, az FM standard error nem megbízható

## Alkalmazás KKE piacokon

**Kihívások:**
- Kis részvényszám (BUX ~20, WIG20 ~20, PX ~14) → portfólióképzés korlátozott
- Rövid idősoros adat (1990-es évek közepe óta megbízható) → T alacsony
- Likviditási szűrés különösen fontos (ritka kereskedés torzítja a bétát)

**Ajánlás:**
- Egyesített KKE panel (Magyarország + Lengyelország + Csehország + Románia) alkalmazása T és N növelésére
- Portfólió-alapú béta becslés (4 portfólió is jobb, mint egyedi részvény béta)
- Shanken-korrekció alkalmazása kötelező

## Kapcsolódó wiki oldalak

- [[source_summaries/fama-macbeth-1973]] — az eredeti paper
- [[source_summaries/shanken-zhou-2006]] — az EIV és Shanken-korrekció szimulációs vizsgálata
- [[source_summaries/fama-french-1992]] — FM alkalmazása size+B/M tesztelésnél
- [[methodology/factor-validation]] — tágabb faktorvalidációs eljárás
- [[open_questions/kke-factor-premiums]] — KKE alkalmazhatóság
