---
type: source_summary
tags: [factor-zoo, multiple-testing, factor-decay, statistics, cross-section, backtesting]
confidence: high
last_reviewed: 2026-04-15
related: [[concepts/factor-decay]], [[concepts/factor-zoo]], [[concepts/multiple-testing]], [[methodology/factor-validation]], [[source_summaries/harvey-liu-zhu-2016]]
---

# McLean & Pontiff (2015) — Does Academic Research Destroy Stock Return Predictability?

**Forrás:** Journal of Finance, 71(1), 5–32, 2016 (online first 2015)  
**Szerzők:** R. David McLean (University of Alberta), Jeffrey Pontiff (Boston College)  
**Fájl:** `raw/raw/AcademicReviewFactor.pdf`

## Fő állítás

Az akadémiai publikáció **elpusztítja** a részvényhozam-előrejelzhetőség jelentős részét: 97 cross-sectional predictor vizsgálatával megmutatják, hogy az out-of-sample hozam 26%-kal, a publikáció utáni hozam 58%-kal csökken az in-sample hozamhoz képest.

## Módszertan

- **Adatbázis:** 97 cross-sectional visszatérési prediktort azonosítanak 80 peer-reviewed cikkből (JF, JFE, RFS)
- **Periódusok:** in-sample (az eredeti cikk mintája), out-of-sample (az eredeti minta vége utáni időszak), post-publication (publikáció után)
- **Portfóliók:** Long-short a legszélső 20-as percentilesek alapján
- **Módszer:** Ugyanazokat a portfóliókat követik végig mind a három periódusban

## Főbb eredmények

| Periódus | Átlagos hozamcsökkenés |
|---|---|
| Out-of-sample (mintán kívül) | −26% |
| Post-publication | −58% |
| Tisztán publikáció-indukált csökkenés | ~−32% (=58%−26%) |

1. **OOS csökkenés (−26%):** A data mining és statisztikai torzítás felső korlátja. Néhány befektető már a publikáció előtt megtudja a predictort.
2. **Post-publication csökkenés (−58%):** A befektetők megtanulják a félreárazást a cikkekből és arbitrálnak → a prémium csökken.
3. **Nagyobb csökkenés magas in-sample hozamnál:** A legmagasabb in-sample hozamú prediktorok csökkennek a legtöbbet — konzisztens a félreárazás hipotézissel.
4. **Likviditás és arbitrázs:** A likvid részvényekben és alacsony idiosynkratikus kockázatú részvényekben a post-publication csökkenés nagyobb → könnyebb arbitrálni.
5. **Korreláció változás:** Publikáció után a predictor portfólió hozama jobban korrelál más már publikált prediktorokkal (és kevésbé a még nem publikáltakkal) — közös mispricing forrás.
6. **Kereskedési aktivitás:** A tárgyalt részvényekben a short interest és a kereskedési volumen növekszik publikáció után → befektetők olvassák és alkalmazzák.

## Elméleti következmények

- A hozam-előrejelzhetőség **legalább részben félreárazásból** ered (nem csak kockázatból), mivel a kockázat alapú prémiumok nem tűnnének el arbitrázzsal
- Az arbitrázs lassú és tökéletlen — a prémium nem tűnik el azonnal
- A Harvey et al. (2016) t > 3.0 küszöbének alkalmazása sem elegendő: ha a cikk megjelenik, az arbitrázs elkezdi erodálni a prémiumot

## Relevanciája a wiki számára

- **Factor zoo kontextus:** Ez az empirikus bizonyíték arra, hogy a [[concepts/factor-zoo]]-ban dokumentált 316+ faktor hozama publikáció után rendszeresen csökken
- **Backtesting validálás:** Minden backtest eredményt korrigálni kell a publikáció-torzítással — [[methodology/backtest-overfitting-detection]] és [[methodology/deflated-sharpe-ratio]] eszközkészletének kiegészítése
- **KKE relevancia:** KKE piacokon a faktor anomáliák lassabban tűnhetnek el (kisebb piac, kevesebb arbitrázs tőke, alacsonyabb likviditás) → a prémiumok tartósabbak lehetnek

## Kapcsolódó wiki oldalak

- [[concepts/factor-decay]] — a jelenség részletes conceptje (ez alapján létrehozva)
- [[concepts/factor-zoo]] — a 316+ faktor probléma
- [[concepts/multiple-testing]] — statisztikai torzítás a faktor irodalomban
- [[methodology/factor-validation]] — a validáció eljárása
- [[source_summaries/harvey-liu-zhu-2016]] — komplementer paper a statisztikai kritikáról
