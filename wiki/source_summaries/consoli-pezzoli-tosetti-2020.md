---
type: source_summary
tags: [gdelt, sentiment, fixed-income, machine-learning, europe]
confidence: medium
last_reviewed: 2026-04-14
related: [[entities/gdelt]], [[concepts/news-sentiment-factor]]
---

# Consoli, Pezzoli & Tosetti (2020) — Using the GDELT Dataset to Analyse the Italian Sovereign Bond Market

## Bibliografia

- **Szerzok:** Sergio Consoli, Luca Tiozzo Pezzoli, Elisa Tosetti
- **Ev:** 2020
- **Kiadó:** Springer, LOD 2020 (Lecture Notes in Computer Science, vol 12565)
- **DOI:** 10.1007/978-3-030-64583-0_18
- **Forras fajl:** `raw/papers/Using the GDELT Dataset to Analyse the Italian Sovereign Bond Market.md`

## Fo allitasok

1. A **GDELT adatbazis** felhasznalhato az **olasz allamkotveny spread** (Olaszorszag vs. Nemetorszag 10 eves hozamkulonbseg) elorejelezkesere.
2. A **GDELT feature-ok hozzaadasa** a klasszikus hozamgorbe-faktorokhoz (level, slope, curvature — Nelson-Siegel) **javitja a credit spread elorejelzest**.
3. **Gradient Boosting Machine (GBM)** modellt hasznaltak a GDELT feature-ok es hozamgorbe faktorok kombinalasara.
4. A GDELT-bol szarmazó szoveges/sentiment feature-ok **komplemenser informaciot** hordoznak a hagyomanyos makro valtozokhoz kepest.

## Modszertan

- **Adatok:** GDELT GKG + Bloomberg olasz/nemet allamkotveny hozamok, 2015. marcius – 2019. augusztus.
- **Fuggó valtozo:** olasz sovereign spread (IT 10Y - DE 10Y).
- **Regresszorok:** Nelson-Siegel faktorok (level, slope, curvature) + GDELT-bol szelektalt feature-ok.
- **Feature engineering:** GDELT GKG-bol kigyujtott tonalitas, media figyelmes es tema-specifikus valtozok, Elasticsearch + Kibana segitsegevel.
- **Modell:** H2O GBM (Gradient Boosting Machine), grid search hiperparameter-optimalizalassal.
- **Osszehasonlitas:** GDELT-bovitett modell vs. klasszikus csak-hozamgorbe modell.

## Relevans eredmenyek a factor trading rendszerhez

- **Europai fixed income kontextus** — ez a forras a GDELT-et europai allampapir-piacra alkalmazza, ami kozelebb all a KKE relevanciahoz mint a kinai vagy amerikai tanulmanyok.
- **GDELT mint kiegeszito faktor** — nem onallo prediktor, hanem a tradicionalis faktorokat egesziti ki.
- **Sovereign spread predikcios** potencial — ez releváns barmelyik kelet-europai allam kotvenypiaci elemzesehez.
- **GBM modell** — nemilinearis osszefuggeseket tud megragadni a sentiment es spread kozott.

## Limitaciok

- Rovid idoszak (2015–2019, ~4.5 ev).
- Csak Olaszorszagra — nincs cross-country validacio.
- A konkrét GDELT feature-ok szelekcioja nem mindig transzparens.
- Nincs trading strategia — csak spread-elorejelzesi pontossag.
- A GBM hiperparameterek grid search-csel tunolva — overfitting kockazat.
