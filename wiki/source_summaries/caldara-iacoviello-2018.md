---
type: source_summary
tags: [geopolitics, sentiment, macro-factor, kke, emerging-markets, time-series, risk]
confidence: high
last_reviewed: 2026-04-15
related: [[entities/gpr-index]], [[entities/gdelt]], [[concepts/monetary-policy-spillover]], [[open_questions/kke-factor-premiums]], [[source_summaries/arteta-kamin-ruch-2022]]
---

# Caldara & Iacoviello (2018) — Measuring Geopolitical Risk

**Forrás:** Federal Reserve IFDP 1222, 2018. február (végleges: American Economic Review, 2022)  
**Szerzők:** Dario Caldara, Matteo Iacoviello (Federal Reserve Board)  
**Fájl:** `raw/raw/ifdp1222.pdf`

## Fő állítás

A **GPR (Geopolitical Risk) index** havi indikátor, amely 11 vezető angol nyelvű újságban számszerűsíti a háborúra, terrorizmusra és államközi feszültségekre utaló cikkek arányát. A magasabb geopolitikai kockázat **csökkenti a reálgazdasági aktivitást, a tőzsdei hozamokat**, és tőkekivonást okoz a feltörekvő gazdaságokból.

## Az index felépítése

### Definíció
Geopolitikai kockázat = háborúk, terrorista cselekmények és olyan államközi feszültségek kockázata, amelyek megzavarják a normális nemzetközi kapcsolatok menetét.

### Mérés
- **11 újság:** Boston Globe, Chicago Tribune, Daily Telegraph, Financial Times, Globe and Mail, Guardian, Los Angeles Times, New York Times, The Times, Wall Street Journal, Washington Post
- **Automatizált szöveges keresés:** 6 kategória kulcsszavai (háborús fenyegetések, nukleáris feszültségek, terrorveszély, tényleges geopolitikai cselekmények stb.)
- **Normalizálás:** 2000–2009 átlaga = 100
- **Két alindex:**
  - **GPT (Geopolitical Threats):** Fenyegetések, feszültségek (Groups 1–4)
  - **GPA (Geopolitical Acts):** Tényleges cselekmények (Groups 5–6)
- **Historikus GPR (GPRH):** 1900-ig visszamenőleg (3 újság)

### Legfontosabb csúcsok (1985–2016)
- Gulf War (1990–91)
- 9/11 (2001)
- Irak invázió (2003) — **maximális csúcs**
- Ukrajna/Oroszország krízis (2014)
- Párizsi terrortámadás (2015)

## Főbb eredmények

### Makrogazdasági hatások (VAR elemzés, US adatok)
- GPR emelkedés → tartós csökkenés: ipari termelés, foglalkoztatás, nemzetközi kereskedelem
- GPR emelkedés → rövid de szignifikáns tőzsdei esés
- **Iparági szétválasztás:** védelmi szektor pozitív excess return; kitett iparágak (acél, bányászat) negatív

### Fenyegetések vs. cselekmények szétválasztása
- **GPA sokkok (tényleges események):** A bizonytalanság megszűnésével kis hatás → "resolution of uncertainty"
- **GPT sokkok (fenyegetések):** Tartós bizonytalanság emelkedés → tartós reálgazdasági visszaesés
- **Következmény:** A befektetők a várható geopolitikai kockázatra reagálnak erősebben, mint a tényleges eseményekre

### Nemzetközi propagáció
- Geopolitikai kockázat → csökkenés 17 ország tőzsdéin (panel adat)
- **Tőkeáramlás:** GPR emelkedés → tőkekivonás EM-ekből, USA és más "safe haven"-ek felé
- Az EM tőzsdék negatív reakciója szignifikáns és perzisztens

## Összehasonlítás GDELT Tone-nal

| Dimenzió | GPR Index | GDELT Tone |
|---|---|---|
| Mit mér | Geopolitikai kockázat specifikusan | Általános médiasentiment |
| Irány | Csak kockázat (negatív irányú) | + és − |
| Frekvencia | Havi (napi is elérhető) | Napi |
| Lefedettség | 11 angol újság | 100+ nyelv, globális |
| Kontextus | Igen (keyword kategóriák) | Nem (szótáralapú) |
| KKE lefedettség | Korlátozott (angol dominancia) | Gyenge |

→ Részletes összehasonlítás: [[comparisons/gdelt-tone-vs-gpr]]

## KKE relevanciája

- **KKE piacok geopolitikai béta-ja magas** — különösen Ukrajna szomszédsága, NATO-feszültségek, Oroszország-szankciók kontextusban
- A GPR 2014-es (Ukrajna/Crimea) és 2022-es csúcsai közvetlenül érintik a KKE régió tőkepiacait
- Az Arteta et al. (2022) "reakciós sokk" koncepciójával kombinálva: GPR emelkedés → reakciós Fed policy kockázat → dupla nyomás KKE-ra
- A GPT (fenyegetések) alindex különösen releváns: az orosz katonai fenyegetés hosszú ideig magas marad anélkül, hogy tényleges esemény következne be

## Limitációk

- Kizárólag angol nyelvű sajtó → KKE regionális geopolitikai kockázatokat alulméri
- "Global" geopolitikai kockázat ≠ KKE-specifikus kockázat
- Nincs country-level GPR KKE országokra (Magyarország, Lengyelország, Csehország)
- A 2022-es Ukrajna-háború hatása az eredeti mintán (1985–2016) kívül esik

## Kapcsolódó wiki oldalak

- [[entities/gpr-index]] — az index részletes entity oldala (ez alapján létrehozva)
- [[entities/gdelt]] — alternatív/komplementer adatforrás
- [[comparisons/gdelt-tone-vs-gpr]] — részletes összehasonlítás
- [[open_questions/kke-factor-premiums]] — KKE geopolitikai kockázat csatorna
