---
type: concept
tags: [sentiment, gdelt, factor-model, time-series, machine-learning]
confidence: medium
last_reviewed: 2026-04-14
related: [[entities/gdelt]], [[concepts/factor-zoo]], [[concepts/factor-cyclicality]], [[source_summaries/shen-xia-shuai-gao-2022]], [[source_summaries/zhang-2025]], [[source_summaries/consoli-pezzoli-tosetti-2020]]
---

# News Sentiment Factor

## Mi ez

A news sentiment factor a hirfolyambol (ujsagcikkek, online media, broadcast) kinyert szoveges tonalitas/hangulat felhasznalasa penzugyi elorejelezkesre es kereskedesi szignalkent. A hagyomanyos faktor modellek (pl. [[entities/fama-french-five-factor-model]]) fundamentalis szamviteli adatokra epulnek — a sentiment factor ezzel szemben **szoveges, nem-strukturalt adatbol** szarmazo informaciot ragad meg.

## Hogyan epul fel

### Adatforrasok

- **GDELT** ([[entities/gdelt]]) — a legelterjedtebb nyilt forrasu hirfolyam adatbazis, 100+ nyelven, napi frissitessel
- **RavenPack** — kereskedelmi NLP-alapu hirszeniment szolgaltatas
- **Mainstream media** (WSJ, NYT, Bloomberg) — hagyomanyos megkozelites, de szuk mertek
- **Social media** (Twitter/X, StockTwits) — zajos, de real-time

### Sentiment metrikai

A forrasaink alapjan a kovetkezo sentiment meroesztozok bizonyultak hasznnosnak:

| Metrika | Leiras | Forras |
|---------|--------|--------|
| **Mean Tone / Sentiment** | Cikkek atlagos tonalitasa | Shen et al. (2022), Zhang (2025) |
| **Sentiment Dispersion** | Tonalitas szórás — nezetelteres merteke | Shen et al. (2022), Zhang (2025) |
| **News Volume / Attention** | Cikkek szama — mediafigyelem | Shen et al. (2022) |
| **Article Impact** | Sentiment * log(volume) | Zhang (2025) |
| **Optimism** | Pozitiv cikkek aranya | Shen et al. (2022) |
| **Emotional Polarity** | Erzelmileg toltott szavak aranya | Shen et al. (2022) |
| **Goldstein Score** | GDELT esemeny-hatas mertek | Zhang (2025) |

### NLP megkozelitesek

- **Lexikon-alapu:** Harvard-IV, Loughran-McDonald sentiment szotarak — egyszeru, de kontextus-erzeketlen
- **FinBERT:** finance-domain pretrained BERT modell — kontextusfuggo, pontosabb (Zhang 2025)
- **GDELT beepitett tone:** a GDELT sajat tonalitas szamitasa ~40 sentiment szotar alapjan

## Fo eredmenyek a forrasokbol

### 1. Kinai reszvenpiac (Shen et al. 2022)
- GDELT GKG-bol epitett sentiment valtozok **szignifikansan** jelzik elore a kinai tozsde hozamait es volatilitasat.
- **Aszimmetrikus hatas:** a piac tulreagalja a negativ hireket.
- EGARCH modellek sentiment-kiterjesztessel javulnak.

### 2. Makro piacok — FX es kotveny (Zhang 2025)
- GDELT + FinBERT + XGBoost → next-day return direction predikció.
- **Sharpe 4.65–5.87** (out-of-sample, de gyanusan magas — replikacio kell).
- A **sentiment dispersion** a legfontosabb feature (SHAP elemzes).

### 3. Olasz allamkotveny (Consoli et al. 2020)
- GDELT feature-ok javitjak a sovereign spread elorejelzeset a hagyomanyos hozamgorbe-faktorokhoz kepest.
- GBM modell — GDELT mint **kiegeszito**, nem onallo prediktor.

## Kulonbseg a hagyomanyos faktoroktol

| Jellemzo | Hagyomanyos faktor (FF5) | News Sentiment Factor |
|----------|-------------------------|----------------------|
| Adat tipusa | Szamviteli (fundamentalis) | Szoveges (NLP) |
| Frekvencia | Honapos/negyedeves | Napi/intraday |
| Cross-section vs time-series | Cross-section ranking | Tobbnyire time-series predikció |
| Elmeleti motivacio | DDM / risk-based | Behavioral (investor sentiment) |
| Decay | Lassu (evek) | Gyors (napok) |

## Nyitott kerdesek

1. **Cross-sectional sentiment faktor:** az eddigi tanulmanyok foleg time-series aggregalt indexeket epitettek. Mukodik-e reszveny-szintu sentiment mint cross-sectional faktor (a la SMB/HML)?
2. **KKE relevancia:** a GDELT-bol szarmazo sentiment predikcios ereje tesztelendo a kelet-europai piacokra — lasd [[open_questions/kke-factor-premiums]].
3. **Overfitting kockazat:** a Zhang (2025) Sharpe-ratok extremen magasak — independent replikacio szukseges.
4. **Sentiment decay:** milyen gyorsan arazodik be a hir? Napon belul, masnapra, vagy lassabban?
5. **GDELT lefedettség:** a KKE mediabazis kicsi a GDELT-ben — eleg-e a signal-to-noise ratio?

## Kapcsolodas az MMCP projekthez

Az MMCP projekt mar hasznalja a GDELT-et geopolitikai szignalkent energia-piacokra. A news sentiment factor megkozelites hasonlo pipeline-t hasznal (GDELT → feature engineering → predikcio), de mas celra: az MMCP konfliktuseseményeket figyel, mig a sentiment factor a tonalitast/hangulatot.
