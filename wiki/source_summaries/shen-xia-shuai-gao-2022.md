---
type: source_summary
tags: [sentiment, gdelt, emerging-markets, time-series, machine-learning]
confidence: medium
last_reviewed: 2026-04-14
related: [[entities/gdelt]], [[concepts/news-sentiment-factor]], [[concepts/factor-zoo]]
---

# Shen, Xia, Shuai & Gao (2022) — Measuring News Media Sentiment Using Big Data for Chinese Stock Markets

## Bibliografia

- **Szerzok:** Shulin Shen, Le Xia, Yulin Shuai, Da Gao
- **Intézmeny:** Huazhong University of Science and Technology / BBVA
- **Ev:** 2022 (Working Paper 22/05)
- **Forras fajl:** `raw/papers/News-Media-Sentiments-from-Big-Data-with-author-info.md`

## Fo allitasok

1. A **GDELT Global Knowledge Graph (GKG)** adatbazisbol epitett **hirsentiment valtozok** szignifikansan elorejelezhetek a kinai tozsde hozamait es volatilitasat.
2. Ot sentiment meroeszkozt epitettek: **Tone** (atlagos hangnem), **Optimism** (pozitiv cikkek aranya), **Attention** (cikkek szama), **Tone Dispersion** (hangnem szórás), **Emotional Polarity** (erzelmi toltottség).
3. **Pozitiv tone es optimizmus** → magasabb jövobeli hozam, alacsonyabb volatilitas.
4. **Tobb mediafigyelmes (attention) es nagyobb tone diszperzio** → alacsonyabb jövobeli hozam, magasabb volatilitas.
5. **Aszimmetrikus sentiment hatasok:** a kinai piac tulreagalja a negativ hireket — kulonosen a Shenzhen toszden.
6. Az **EGARCH modellek** sentiment valtozokkal szignifikansan javitjak az elorejelzesi pontossagot.

## Modszertan

- **Adatforras:** GDELT GKG, 2015-tol, Google BigQuery-vel lekerdezve.
- **Szuresek:** Kinabol szarmazo hirek, "Stock Market", "IPO", "Economic Bubble" temakkal.
- **Sentiment dictionaryk:** 40+ finomsagi szotar (Harvard-IV, Loughran-McDonald, Fed Financial Stability).
- **Modell:** EGARCH (Nelson, 1991) sentiment kiterjesztessel.

## Relevans eredmenyek a factor trading rendszerhez

- **GDELT mint faktor adat:** ez az elso tanulmany, ami a GDELT-bol szisztematikusan epit hirszeniment faktorokat tozsdeindex-elojelzesre.
- **Nem cross-sectional faktor** hanem **time-series prediktor** — a sentiment nem a reszvenyeket rangsorolja, hanem az aggregalt piaci hozamot jelzi eloer.
- **KKE relevancia:** ha a GDELT Kinaban mukodik (speculative market, gyenge intezmenyek), a KKE piacokra is tesztelheto.
- **Tone Dispersion** kulonosen erdekes — a nezetelteres mint volatilitas-prediktor.
- A GDELT-bol szarmazo sentiment megbypassolja a mainstream media szelekcios torzitast.

## Limitaciok

- Csak aggregalt piaci szintu elemzes — nincs reszvenyszintu cross-section.
- A GKG adatbazis 2015-tol indult — rovid idosor.
- A Kina-specifikus eredmenyek nem feltetlenul transferalhatoak mas piacokra.
- Nincs out-of-sample trading strategia — csak statistikai szignifikancia.
