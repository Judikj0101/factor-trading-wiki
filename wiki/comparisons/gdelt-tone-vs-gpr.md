---
type: comparison
tags: [gdelt, geopolitics, sentiment, macro-factor, data-source, kke]
confidence: high
last_reviewed: 2026-04-15
related: [[entities/gdelt]], [[entities/gpr-index]], [[source_summaries/caldara-iacoviello-2018]], [[source_summaries/shen-xia-shuai-gao-2022]], [[open_questions/kke-factor-premiums]]
---

# GDELT Tone vs Caldara-Iacoviello GPR Index

## Összefoglalás

| Dimenzió | GDELT Average Tone | GPR Index |
|---|---|---|
| **Mit mér** | Általános média-hangulat (pozitív + negatív) | Geopolitikai kockázat (fenyegetések + cselekmények) |
| **Irány** | Kétirányú: –100 (negatív) → +100 (pozitív) | Egyirányú: 0-tól felfelé (kockázat növekszik) |
| **Fókusz** | Minden téma (gazdaság, politika, társadalom, kultúra) | Kizárólag háború, terrorizmus, államközi feszültségek |
| **Forrás** | 100+ nyelv, online/print/broadcast globálisan | 11 vezető angol újság |
| **Felbontás** | Napi (15 perces frissítés) | Havi |
| **Idősor** | 1979-től (Event DB), 2015-től (GKG) | 1985-tól (benchmark), 1900-tól (GPRH) |
| **Hozzáférés** | Ingyenes (BigQuery, CSV) | Ingyenes (szerzők weboldalán) |
| **Normalizálás** | Nincs standard; relatív változások számítanak | 2000–2009 átlaga = 100 |

## Részletes összehasonlítás

### 1. Mérési cél

**GDELT Tone** az összes média-tartalom érzelmi töltetét méri — beleértve a pozitív eseményeket (gazdasági növekedés, diplomáciai sikerek) is. Egy csökkent GDELT Tone értéke nem feltétlenül jelent geopolitikai kockázatot — lehet recessziós félelem, skandalum, társadalmi feszültség is.

**GPR Index** kizárólag a háborús fenyegetés és geopolitikai cselekmények médiajelenlétét méri hat kulcsszókategórián keresztül. Magasabb GPR = több geopolitikai félelem, de semmi más.

**Következmény a faktor kutatásban:** GDELT Tone általánosabb sentiment proxy; GPR specifikus kockázat-indikátor. Egy faktormodellben mindkettő bevonható, de multikollinearitást okozhat — különösen geopolitikai válságok idején erősen korrelálnak.

### 2. Időbeli felbontás

A GDELT napi felbontású — rövid ablakú event study-khoz alkalmasabb (pl. választási napok, kamatdöntések előtt/után). A GPR havi — inkább medium-term makro rezsim azonosítására használható.

**KKE alkalmazás:** Ha havi hozamot magyarázunk, a GPR közvetlenül felhasználható regresszióban. A GDELT napi adatait havi aggregátummá kell alakítani (átlag, szórás, maximum) — ezzel információ vész el.

### 3. Tartalom: gépi tanulás vs. szótáralapú

| | GDELT Tone | GPR |
|---|---|---|
| **Módszer** | Szótáralapú (40+ dictionary, pl. Harvard-IV, Loughran-McDonald) | Kulcsszó-keresés (6 kategória, ~10 kulcsszócsoport) |
| **NLP szint** | Alap — nem kontextusfüggő | Nagyon alap — boolean keresés |
| **Fejlesztési lehetőség** | FinBERT vagy LLM-alapú hangulatelemzés (Zhang 2025) | Korlátozott; fix definíció az összehasonlíthatóság érdekében |

A Zhang (2025) megközelítés pont emiatt váltja fel a nyers GDELT Tone-t FinBERT-tel — a szótáralapú módszer kontextust nem érzékel (pl. "no war" pozitívként olvasható).

### 4. Lefedettség és torzítás

**GDELT:** 100+ nyelv, globális média — de erős angol/nyugati dominancia. A KKE régió (Magyar, Lengyel, Cseh sajtó) alulreprezentált lehet, kivéve a nagy angolszász lapok KKE-tudósításait.

**GPR:** 11 angol újság, mind nyugati — ugyanolyan torzítással, de kisebb portfólióból. Viszont a 11 lap geopolitikailag megbízható forrás; a keresett témák globálisan zajló eseményeket fednek le (amelyeket az angolszász lapok jellemzően jól lefednek).

**KKE-specifikus következmény:** Mindkét index tükrözi a globális geopolitikai percepciókat, de nem feltétlenül a KKE-specifikus helyi kockázatokat (pl. lengyel belpolitika, magyar jegybanki döntések). Ezek mérésére lokális sajtó vagy egyéb adatforrás szükséges.

### 5. Pénzügyi hatások az irodalom alapján

| Esemény | GDELT Tone hatás | GPR hatás |
|---|---|---|
| Geopolitikai válság | Tone csökken (negatív) | GPR megugrás |
| Recessziós félelem | Tone csökken, GPR stabil | GPR stabil |
| Diplomáciai siker | Tone emelkedik | GPR csökken (mérsékelten) |
| Választás/politikai bizonytalanság | Tone vegyes | GPR általában stabil |

**Tőkepiac hatás (GPR, Caldara-Iacoviello 2018):**
- GPR megugrás → tőkekiáramlás EM-ekből, alacsonyabb gazdasági aktivitás
- GPT (threats) hatása tartósabb mint GPA (acts) — a piacok a fenyegetésre reagálnak, nem csak a tényekre

**Részvénypiac hatás (GDELT, Shen et al. 2022):**
- GKG Tone szignifikáns prediktív erő a kínai tőzsdeindexre
- EGARCH modellben: negatív Tone → magasabb volatilitás

### 6. Mikor melyiket használd?

| Cél | Javasolt |
|---|---|
| Geopolitikai kockázat regresszorként havi frekvencián | **GPR** |
| Általános sentiment faktor napi frekvencián | **GDELT Tone / GKG** |
| Rövid ablakú event study (napok) | **GDELT** |
| Rezsimdetekció (háborús vs. békés időszak) | **GPR** (GPT alindex) |
| Globális makro kockázat kontrollváltozó | **GPR** |
| NLP pipeline inputja FinBERT-hez | **GDELT** (nyers szöveg) |
| KKE factor prémium magyarázata | **GPR** (elsősorban) + GDELT (kiegészítőként) |

## Összefoglalás

**GPR** a jobb választás ha geopolitikai kockázat specifikus hatását akarod izolálni. Havi, pontosan definiált, replikálható, peer-reviewed forrásból.

**GDELT Tone** akkor hasznos, ha általánosabb sentiment faktort keresel napi felbontásban, vagy ha NLP pipeline bemeneteként használod. De nyers formájában erős torzításokkal terhelt.

**Kombinált használat** elvben lehetséges — de multikollinearitás kezelése szükséges (VIF ellenőrzés, ortogonalizálás, vagy szeparált regressziók).

## Kapcsolódó oldalak

- [[entities/gdelt]] — GDELT adatbázis részletes leírása
- [[entities/gpr-index]] — GPR Index részletes leírása
- [[source_summaries/caldara-iacoviello-2018]] — GPR eredeti papere
- [[source_summaries/shen-xia-shuai-gao-2022]] — GDELT részvénypiaci alkalmazás
- [[open_questions/kke-factor-premiums]] — KKE kontextusban melyik a relevánsabb?
