---
type: entity
tags: [macro-factor, bond-yields, monetary-policy, risk-premium, time-series]
confidence: high
last_reviewed: 2026-04-15
related: [[entities/market-risk-premium]], [[entities/beta]], [[concepts/monetary-policy-spillover]], [[source_summaries/adrian-gelos-lamersdorf-moench-2024]], [[source_summaries/arteta-kamin-ruch-2022]]
---

# Term Premium (Lejárati kockázati prémium)

## Definíció

A hosszú lejáratú kötvény hozama két komponensre bontható:

$$y^{(n)}_t = \underbrace{\frac{1}{n}\sum_{i=0}^{n-1} E_t[r_{t+i}]}_{\text{várható rövid kamatok}} + \underbrace{TP^{(n)}_t}_{\text{term premium}}$$

A **term premium** az a hozamtöbblet, amelyet a befektetők a hosszú lejáratú kötvény tartásáért követelnek a rövid lejáratúhoz képest, a kamatozás bizonytalansága és a tartási kockázat miatt.

- Ha a piac biztos a kamatpályában → term premium alacsony
- Ha nagy a bizonytalanság (pl. infláció, politika) → term premium magas

## Mérése

A legszélesebb körben használt mérési módszer: **Adrian, Crump & Moench (2013) 3-faktor affin term structure modell** (ACM modell), amelyet a Fed NY publikál.

$$TP^{(10Y)}_t = y^{(10Y)}_t - E_t\left[\overline{r}_{short}\right]_{0 \to 10Y}$$

## Viselkedése monetáris politikai sokkokra

Adrian et al. (2024) alapján:

| Időszak | Fed szigorítás | Fed lazítás |
|---|---|---|
| Pre-GFC (–2007) | TP emelkedik (tartósan) | TP erősen emelkedik (ellensúlyozza a kamatcsökkentést!) |
| Post-GFC (2010–) | TP csökken (reversal) | TP csökken (tartósan) |

**Kulcslelet:** Pre-GFC-ban a Fed lazítási sokkokat ellensúlyozta a term premium emelkedése — ezért a hosszú hozamok alig csökkentek. Post-GFC-ban ez megfordult: mind szigorítás, mind lazítás után a term premium csökken.

## Kapcsolata faktor tradinghez

1. **Makro faktor:** A term premium szintje és változása makro tényezőként beépíthető cross-sectional faktor modellbe — különösen pénzügyi szektorra, hosszú duration-ú részvényekre (utility, REIT).
2. **KKE relevancia:** A KKE szuverén kötvények term premiuma az US Treasury term premium dinamikáját követi (Adrian et al. 2024 szerint az EM hozamok utánozzák az US mintát). Reakciós Fed sokknál a KKE term premium emelkedik → kötvény drawdown → tőkekivonás → részvénypiaci nyomás.
3. **Duration kockázat:** Hosszú duration portfólióknál (pl. quality/growth részvények) a term premium emelkedése negatív korreláción keresztül hat az értékelésekre.

## Adatforrások

- **ACM Term Premium:** Federal Reserve Bank of New York ([link](https://www.newyorkfed.org/research/data_indicators/term-premia-on-us-treasury-securities))
- **BIS adatok:** Adrian et al. (2024) szuverén kötvényhozam dekompozíció fejlett és feltörekvő piacokra

## Limitációk

- Modell-függő: különböző term structure modellek különböző term premium értékeket adnak
- Rövid idősora a feltörekvő piaci dekompozíciónak
- KKE-specifikus term premium mérés nem publikusan elérhető

## Kapcsolódó oldalak

- [[entities/market-risk-premium]] — részvénykockázati prémium analógiája
- [[concepts/monetary-policy-spillover]] — hogyan terjed a Fed hatása globálisan
- [[source_summaries/adrian-gelos-lamersdorf-moench-2024]] — fő forrás
- [[open_questions/kke-factor-premiums]] — KKE kontextus
