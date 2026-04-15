---
type: source_summary
tags: [methodology, cross-section, statistics, fama-macbeth, regression]
confidence: high
last_reviewed: 2026-04-15
related: [[methodology/fama-macbeth-regresszio]], [[source_summaries/fama-macbeth-1973]], [[entities/capm]], [[entities/beta]]
---

# Shanken & Zhou (2006) — Estimating and Testing Beta Pricing Models

**Forrás:** NBER Working Paper 12055, 2006. február  
**Szerzők:** Jay Shanken (Emory), Guofu Zhou (Washington University in St. Louis)  
**Fájl:** `raw/raw/w12055.pdf`

## Fő állítás

Szimulációs vizsgálatban összehasonlítják a **Fama-MacBeth (FM) kétlépéses eljárást**, a maximum likelihood (ML) és a GMM becslőket cross-sectional várható hozam modellek tesztelésénél. Az OLS-FM becslő megbízható inferenciát ad, de kevésbé precíz; a GLS-FM precízebb, de torzítottabb.

## Főbb eredmények

1. **OLS-FM:** Megbízható szignifikancia tesztek, de nagy szórású becslések — alkalmas inferenciára, nem pontbecslésre
2. **GLS-FM:** Pontosabb becslések, de **szisztematikus torzítás** → nem megbízható t-statisztikák
3. **"Csonkított" ML:** A legjobb kompromisszum bias és precizitás között — de az OLS-FM-nél kevésbé megbízható inferenciában
4. **Model misspecification:** Aszimptotikus eloszlásra vonatkozó új eredmények modell-misspecifikáció esetén
5. **Eltérő becslők viszonya:** Analitikus összefüggések az OLS-FM, GLS-FM és ML becslők között

## Praktikus következmények a Fama-MacBeth alkalmazáshoz

- **Ajánlás:** OLS-FM alkalmazása, ha az inferencia (szignifikancia teszt) az elsődleges cél
- **EIV korrekció:** A Shanken (1992) korrekció az FM standard errorokra szükséges a béta becslési hibájának figyelembevételéhez:
$$SE_{Shanken} = SE_{FM} \times \sqrt{1 + \hat{\lambda}^2 / \hat{\sigma}^2_M}$$
- **Portfóliók vs. egyedi részvények:** Portfóliók alkalmazása csökkenti az EIV problémát, de elvész keresztmetszeti variancia

## Relevanciája a wiki számára

- Technikai alap a [[methodology/fama-macbeth-regresszio]] módszertani oldalhoz
- Megindokolja, miért kell a Shanken-korrekt standard errorokat alkalmazni az FM regresszióban
- A KKE faktor tesztelésnél: kis mintával (kevés részvény) az EIV probléma súlyosabb → portfólió-alapú FM ajánlott

## Kapcsolódó wiki oldalak

- [[methodology/fama-macbeth-regresszio]] — az FM eljárás részletes leírása
- [[source_summaries/fama-macbeth-1973]] — az eredeti FM paper
