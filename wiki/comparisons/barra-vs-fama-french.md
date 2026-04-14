---
type: comparison
tags: [factor-model, regression, risk-management]
confidence: high
last_reviewed: 2026-04-14
related: [[entities/barra-risk-model]], [[entities/fama-french-five-factor-model]], [[entities/msci-facs]]
---

# Barra vs Fama-French: két megközelítés a faktor modellezéshez

## Összefoglalás

Mindkettő multi-factor modell, de eltérő céllal, módszertannal és felhasználási területtel.

## Részletes összevetés

| Dimenzió | Barra | Fama-French |
|---|---|---|
| **Eredet** | Barr Rosenberg (1974), ipari | Fama & French (1992, 1993), akadémiai |
| **Fő cél** | Portfólió kockázat előrejelzés | Asset pricing tesztelés, anomáliák |
| **Faktor hozam becslés** | Cross-sectional WLS regresszió | Long-short portfólió sortolás |
| **Faktorok száma** | ~60+ (industry + style + country) | 3–5 |
| **Frissítés** | Napi | Havi |
| **Output** | Kovariancia mátrix, exposure-k, specific risk | Faktor hozam time series |
| **Elérhetőség** | Fizetős (MSCI licensz) | Publikus (Ken French website) |
| **Tipikus felhasználó** | Intézményi portfólió menedzser, risk manager | Akadémiai kutató, quant |
| **Földrajzi lefedettség** | Globális (GEM), lokális (USE, JPN, stb.) | US, majd nemzetközi |

## Módszertani különbségek

### Faktor hozam becslés

**Fama-French:** portfólió sortolás
1. Részvényeket size × B/M alapján portfóliókba sortolják
2. Long-short portfólió hozam = faktor hozam
3. Előny: egyszerű, intuitív, reprodukálható
4. Hátrány: a sortolás dimenziójának megválasztása szubjektív

**Barra:** cross-sectional regresszió
1. Minden részvény exposure-ját ismerjük (industry, style descriptors)
2. Minden nap cross-sectional regresszió: $r_i = \sum X_{ik} f_k + u_i$
3. A regresszió együtthatói ($f_k$) = faktor hozamok
4. Előny: egyszerre sok faktor, nincs information loss a sortolásból
5. Hátrány: modell-függő, a faktor definíciók nem triviálisak

### Faktorok jellege

**Fama-French:** néhány, jól definiált, elméleti motivációjú faktor
- Market, SMB, HML, RMW, CMA (+ opcionálisan MOM)
- Cél: magyarázzák a cross-section hozam variációt

**Barra:** sok faktor, kockázat-modellezési céllal
- Style faktorok (hasonlóak az FF faktorokhoz)
- Industry faktorok (GICS alapú, ~50+)
- Country/market faktorok
- Cél: a lehető legjobb kovariancia mátrix becslés

## Mikor melyiket használjuk

| Feladat | Javasolt megközelítés |
|---|---|
| Új faktor/anomália akadémiai tesztelése | Fama-French |
| Portfólió kockázat mérés és optimalizálás | Barra |
| Mutual fund alpha mérés | Fama-French (Carhart 4F) |
| Risk attribution és reporting | Barra |
| Factor investing stratégia backteszt | Mindkettő — FF az alpha teszthez, Barra a kockázathoz |
| Saját faktor kutatás (publikus adattal) | Fama-French (ingyenes) |

## A kettő nem ellentmondás

A Barra és Fama-French faktorok **ugyanazt a jelenséget** mérik, más módszertannal. Az MSCI FaCS keretrendszer ([[entities/msci-facs]]) a Barra faktorokat használja, de a 8 faktor csoport megfeleltethető az FF faktoroknak.

## Források

- [[source_summaries/barra-risk-model-handbook]]
- [[source_summaries/barra-use4-2011]]
- [[source_summaries/fama-french-2014]]
- [[source_summaries/bender-nielsen-2010]]
