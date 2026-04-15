---
type: entity
tags: [geopolitics, sentiment, macro-factor, kke, emerging-markets, time-series]
confidence: high
last_reviewed: 2026-04-15
related: [[entities/gdelt]], [[concepts/monetary-policy-spillover]], [[open_questions/kke-factor-premiums]], [[source_summaries/caldara-iacoviello-2018]], [[comparisons/gdelt-tone-vs-gpr]]
---

# GPR Index (Geopolitical Risk Index)

## Definíció

A **Caldara & Iacoviello (2018)** által fejlesztett havi geopolitikai kockázat index, amely 11 vezető angol nyelvű újságban automatizált szöveges kereséssel méri a háborúra, terrorizmusra és államközi feszültségekre utaló cikkek arányát.

$$GPR_t = \frac{\text{Geopolitikai cikkek száma}_t}{\text{Összes cikk száma}_t} \times \text{normalizálás}$$

**Normalizálás:** 2000–2009 átlaga = 100.

## Komponensek

| Alindex | Tartalom | Felhasználás |
|---|---|---|
| **GPT** (Geopolitical Threats) | Fenyegetések, feszültségek (Groups 1–4) | Előretekintő kockázat |
| **GPA** (Geopolitical Acts) | Tényleges cselekmények (Groups 5–6) | Realizált sokkok |
| **GPR** (benchmark) | GPT + GPA kombinálva | Általános geopolitikai szint |
| **GPRH** (historikus) | 1900-ig visszamenőleg, 3 újság | Hosszú idősor |

## Újságok (11 db)

Boston Globe, Chicago Tribune, Daily Telegraph, Financial Times, Globe and Mail, Guardian, Los Angeles Times, New York Times, The Times, Wall Street Journal, Washington Post

## Főbb csúcsok

- Gulf War (1990–91)
- 9/11 (2001)
- Irak invázió (2003) — **abszolút maximum**
- Ukrajna/Crimea (2014)
- Párizsi terrortámadás (2015)
- Orosz invázió Ukrajna ellen (2022) — az eredeti minta utáni csúcs

## Gazdasági hatások

A GPR emelkedése:
- ↓ ipari termelés, foglalkoztatás, kereskedelem (tartós)
- ↓ részvényhozamok (rövid, de szignifikáns)
- **Tőkekivonás EM-ekből** → safe haven (USA, CHF) felé
- **GPT sokkok tartósabbak**, mint GPA sokkok (uncertainty channel dominál)

## Összehasonlítás GDELT Tone-nal

| Dimenzió | GPR | GDELT Tone |
|---|---|---|
| Témakör | Csak geopolitika | Minden |
| Irány | Csak kockázat | + és − |
| Frekvencia | Havi (napi is) | Napi |
| Lefedettség | 11 angol újság | 100+ nyelv |
| KKE lefedettség | Gyenge | Nagyon gyenge |

→ Részletes: [[comparisons/gdelt-tone-vs-gpr]]

## Elérhetőség

- **Adatok:** https://www2.bc.edu/matteo-iacoviello/gpr.htm (publikusan elérhető)
- **Frissítés:** havi, valós idejű
- **Napi változat:** szintén elérhető

## Limitációk

- Angol sajtó dominancia → regionális KKE geopolitikai kockázatot alulmér
- Globális index ≠ KKE-specifikus kockázat (Közel-Kelet, Ázsia eseményei torzítanak)
- Nincs country-level GPR Magyarországra, Lengyelországra, Csehországra

## Kapcsolódó oldalak

- [[entities/gdelt]] — komplementer adatforrás, más dimenzióban
- [[source_summaries/caldara-iacoviello-2018]] — fő forrás
- [[comparisons/gdelt-tone-vs-gpr]] — részletes összehasonlítás
- [[concepts/monetary-policy-spillover]] — GPR és Fed reaktív policy kapcsolata
- [[open_questions/kke-factor-premiums]] — KKE geopolitikai kockázati prémium
