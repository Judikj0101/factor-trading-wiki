---
type: entity
tags: [gdelt, sentiment, data-source, machine-learning, global]
confidence: high
last_reviewed: 2026-04-14
related: [[concepts/news-sentiment-factor]], [[open_questions/kke-factor-premiums]], [[source_summaries/shen-xia-shuai-gao-2022]], [[source_summaries/zhang-2025]], [[source_summaries/consoli-pezzoli-tosetti-2020]]
---

# GDELT (Global Database of Events, Language, and Tone)

## Definicio

A GDELT Project egy nyilt hozzaferesu, valós ideju, nagy lepetkeu adatbazis, amely a vilag broadcast, print es online mediat monitorozza. 100+ nyelven dolgoz fel hireket, napi frissitessel, es ingyenesen hozzaferheto kutatasra es kereskedelmi felhasznalasra.

- **Weboldal:** https://www.gdeltproject.org/
- **Hozzaferes:** Google BigQuery, nyers CSV fajlok, API
- **Indulas:** 1979-tol (Event DB), 2015-tol (GKG)

## Ket fo adatbazis

### 1. Event Database

- **Tartalom:** Georeferalt tarsadalmi esemenyek, 300+ kategoriaban (CAMEO koddal kodolva).
- **Idosor:** 1979-tol.
- **Mezok:** dátum, szereplok (Actor1, Actor2), esemeny tipus (EventCode), Goldstein skala (esemeny hatas), forras URL, cikkek szama.
- **Felhasznalás a factor research-ben:** Zhang (2025) az EventCode 100–199 (gazdasagi/diplomáciai esemenyek) szuresevel epit sentiment indexet.

### 2. Global Knowledge Graph (GKG)

- **Tartalom:** Cikk-szintu erzelmi es tematikus elemzes — 2300+ emocio/tema azonositasa minden cikkben.
- **Idosor:** 2015-tol.
- **Mezok:** cikk tone (atlagos tonalitas), pozitiv/negativ szavak szama, temak, szervezetek, helyszinek.
- **Sentiment dictionaryk:** 40+ szotar (Harvard-IV, Loughran-McDonald, WordNet-Affect, Fed Financial Stability).
- **Felhasznalás:** Shen et al. (2022) es Consoli et al. (2020) a GKG-bol epitik a sentiment valtozokat.

## GDELT a factor research-ben

### Equity piac (Shen et al. 2022)
- Kinai tozsdeindexre epitett 5 sentiment metrika (Tone, Optimism, Attention, Dispersion, Polarity).
- EGARCH modellben szignifikans prediktiv ero.
- Lasd: [[source_summaries/shen-xia-shuai-gao-2022]]

### Makro piacok — FX, fixed income (Zhang 2025)
- GDELT v2 + FinBERT → napi sentiment index → XGBoost → next-day return direction.
- EUR/USD, USD/JPY, ZN (Treasury) — Sharpe 4.65–5.87 (OOS, de gyanúsan magas).
- Lasd: [[source_summaries/zhang-2025]]

### Europai sovereign bond (Consoli et al. 2020)
- Olasz allamkotveny spread elorejelezes GDELT feature-okkal + Nelson-Siegel hozamgorbe faktorok.
- GBM modell — a GDELT javitja a klasszikus modellt.
- Lasd: [[source_summaries/consoli-pezzoli-tosetti-2020]]

## Kulcsfontossagu GDELT metrikai

| Metrika | Leiras | Hasznalat |
|---------|--------|-----------|
| **Average Tone** | Cikk atlagos tonalitasa (-100-tol +100-ig) | Alap sentiment mertek |
| **Goldstein Scale** | Esemeny hatásanak merteke (-10-tol +10-ig) | Geopolitikai impact |
| **Num Articles** | Egy esemenyt lefedo cikkek szama | Media attention proxy |
| **CAMEO EventCode** | Standardizalt esemeny-tipizalas | Szures/kategorizalas |

## GDELT az MMCP projektben

Az MMCP (Multi-Modal Conflict Predictor) projekt szinten a GDELT-et hasznalja fo adatforraskent, de mas celra: geopolitikai **konfliktus-esemenyek** detektalasara energia-piacokra vonatkozoan. A GDELT ket felhasznalasi modja:
- **Event-based:** MMCP — specifikus konfliktus-esemenyek azonositasa (CAMEO kodok)
- **Sentiment-based:** factor trading — aggregalt tonalitas/hangulat mint piaci prediktor

## Limitaciok

- **Nyelvi lefedettuseg egyenlotlen:** angol-dominaltas; a KKE media alulreprezentalt lehet.
- **Torzitasok:** a GDELT nem minden forras egyenlo sulyú — a mainstream media dominat.
- **Tone szamitas:** a beepitett tone egyszeru szotar-alapu — nem kontextusfuggo (ezert Zhang FinBERT-et hasznal rá).
- **Lag:** a GKG napi frissitesu — intraday kereskedesre nem alkalmas.
- **Adat mennyiseg:** a GKG 2015-tol indult — rovid idosor regressziohoz.
- **False positives:** a GDELT esemeny-felismero algoritmusa nem tokeletes — duplikaciok, misclassification.

## Elerheto API-k es eszkozok

- **Google BigQuery:** a teljes GDELT archivum lekertheto SQL-lel (ingyenes kvota-ig).
- **GDELT DOC API:** cikk-szintu kereses.
- **GDELT Analysis Service:** vizualizacio es trending.
- **Nyers fajlok:** 15 percenkent frissulo CSV archivum.

## Összehasonlítás GPR indexszel

A GDELT Tone és a Caldara-Iacoviello GPR index különböző dimenziókat mérnek — részletes összevetés: [[comparisons/gdelt-tone-vs-gpr]], entitás: [[entities/gpr-index]]

Rövid összefoglalás: GPR = geopolitikailag specifikus, havi, csak kockázatot mér; GDELT = általános sentiment, napi, pozitív és negatív is.
