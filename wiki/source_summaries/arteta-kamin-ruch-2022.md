---
type: source_summary
tags: [macro-factor, monetary-policy, emerging-markets, kke, financial-crisis, global, regression]
confidence: high
last_reviewed: 2026-04-15
related: [[concepts/monetary-policy-spillover]], [[entities/term-premium]], [[open_questions/kke-factor-premiums]], [[source_summaries/adrian-gelos-lamersdorf-moench-2024]]
---

# Arteta, Kamin & Ruch (2022) — Hogyan hat az USA kamatszint-emelés a feltörekvő és fejlődő gazdaságokra? Attól függ.

**Forrás:** World Bank Policy Research Working Paper No. 10258, 2022. december  
**Szerzők:** Carlos Arteta (World Bank), Steven Kamin (AEI), Franz Ulrich Ruch (World Bank)  
**Fájl:** `raw/raw/IDU032d1feef0db0d0480e0b3190f92d87c50de8.pdf`

## Fő állítás

Az USA kamatemelés hatása a feltörekvő és fejlődő gazdaságokra (EMDE-k) **nem egységes** — a hatás kritikusan függ attól, hogy milyen *típusú sokk* húzódik meg a kamatemelés mögött:

| Sokk típusa | Definíció | EMDE hatás |
|---|---|---|
| **Reál sokk** | Erősebb US gazdasági kilátások | Kedvező |
| **Inflációs sokk** | Emelkedő inflációs várakozások | Káros |
| **Reakciós sokk** | Hawkish Fed irányváltás percepciója | Erősen káros |

## Módszertan

### 1. VAR-alapú sokkdekompozíció
- Sign-restricted Bayesian VAR sztochasztikus volatilitással
- 4 változó: 2Y és 10Y US Treasury hozam, S&P 500, breakeven inflációs várakozás
- Azonosítási stratégia jel-restrikciókkal:
  - Reál sokk: ↑ hozam, ↑ részvény, ↑ infláció
  - Inflációs sokk: ↑ hozam, ↓ részvény, ↑ infláció
  - Reakciós sokk: ↑ hozam, ↓ részvény, ↓ infláció
- Minta: 1982–2022 havi adat

### 2. Panel lokális projekciók (EMDE hatásbecslés)
- Jordà (2005) módszer, 8 negyedév horizont
- 17–38 EMDE, 1997Q4–2019Q4
- Függő változók: helyi devizás kötvényhozam, szuverén spread, tőkebeáramlás, árfolyam, GDP, infláció, kormányzati mérleg

### 3. Logit modell (válságvalószínűség)
- 139 EMDE, 1985–2018 éves adat
- Válságtípusok: deviza-, banki, szuverén adósságválság
- Forrás: Laeven & Valencia (2020)

## Főbb eredmények

### Inflációs és reakciós sokkokra
- ↑ helyi devizás kötvényhozamok, ↑ szuverén spread
- ↓ részvényárak, devizaleértékelés, ↓ tőkebeáramlás
- Kormányzatok megszorítanak: ↑ elsődleges egyenleg, ↓ kiadások, ↓ GDP
- Reakciós sokkokra: **↓ magánfogyasztás és beruházás is**

### Reál sokkokra
- ↓ dollárdenominált szuverén spread
- ↑ részvényárak, reálfelértékelés, ↑ export, ↑ tőkebeáramlás
- Javuló adóbevételek → jobb költségvetési egyenleg

### Válságvalószínűség
- **Reakciós sokk** szinte megduplázza egy EMDE válságba kerülésének valószínűségét
- 25bp reakciós sokk: 3,5% → 6,6% (egy éves horizonton)
- 2022-ben a reakciós sokkokból +114bp 2Y hozam → becsült EMDE válságvalószínűség ~40%-ra nőtt
- **Devizaválság** kockázata a legszigorúbb: reakciós sokk esetén egyértelműen szignifikáns

## Relevanciája a faktor trading wiki számára

**Közvetlen relevancia: nagyon magas** a KKE faktor kutatáshoz.

1. **KKE mint EMDE:** Magyarország, Lengyelország, Csehország mind az EMDE kategóriába esik (Lengyelország investment grade, Magyarország sub-IG peremen). A reakciós sokkok ezeken a piacokon **rendkívül erős drawdownt** okozhatnak.

2. **Faktor dinamika rezsimek szerint:** A sokkdekomponálás keretrendszere alkalmazható KKE részvényfaktor vizsgálatokhoz:
   - Reakciós sokk rezsimben: erős kockázati prémium emelkedés → value faktor relatív vonzerő nő, momentum összeomlik
   - Reál sokk rezsimben: az EMDE piacok a US növekedéssel együtt mozognak → quality/growth faktorok dominálnak

3. **Válságvalószínűség előjelzésre:** A sokkdekompozíciós módszer (VAR + jel-restrikciók) adaptálható KKE-specifikus rezsimdetekciós modellhez — kötvénypiac + részvénypiac + inflációs várakozás együttes figyelése.

4. **Módszertan:** A sign-restricted Bayesian VAR keret a legtisztább publikált keretrendszer az US kamatsokkek azonosítására → referenciaként alkalmazható KKE faktor regressziókban kontrollváltozóként.

## Limitációk

- Az EMDE minta főleg Latin-Amerika és Ázsia — KKE specifikus eredmény nem elkülönítve
- Investment grade vs. non-IG csoportbontás rendelkezésre áll, de country-level KKE eredmény nincs
- Negyedéves frekvencia — részvényfaktor vizsgálathoz magasabb frekvencia kell

## Kapcsolódó wiki oldalak

- [[concepts/monetary-policy-spillover]] — a sokkdekompozíciós keretrendszer
- [[entities/term-premium]] — a 10Y–2Y hozamkülönbség komponensei
- [[open_questions/kke-factor-premiums]] — reakciós sokkok és KKE drawdown kapcsolata
- [[source_summaries/adrian-gelos-lamersdorf-moench-2024]] — komplementer BIS paper (mechanizmus)
