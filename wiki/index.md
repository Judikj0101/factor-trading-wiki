---
type: index
last_updated: 2026-04-14
---

# Factor Trading Wiki — Index

## Entities
_Konkrét módszerek, mutatók, adatforrások, modellek._

### Faktor modellek
- [[entities/capm]] — Capital Asset Pricing Model (Sharpe 1964)
- [[entities/fama-french-five-factor-model]] — FF5: Market + SMB + HML + RMW + CMA
- [[entities/carhart-four-factor-model]] — Carhart 4F: FF3 + Momentum
- [[entities/barra-risk-model]] — Barra/MSCI multi-factor kockázati modell (USE1–USE4, GEM)
- [[entities/msci-facs]] — MSCI FaCS: 8 faktor csoport szabvány

### Faktorok
- [[entities/market-risk-premium]] — $R_M - R_F$, piaci kockázati prémium
- [[entities/smb]] — Size faktor (Small Minus Big)
- [[entities/hml]] — Value faktor (High Minus Low B/M)
- [[entities/rmw]] — Profitability faktor (Robust Minus Weak)
- [[entities/cma]] — Investment faktor (Conservative Minus Aggressive)
- [[entities/momentum]] — Momentum faktor (12-2 havi hozam)
- [[entities/low-volatility]] — Low Volatility faktor
- [[entities/quality-factor]] — Quality faktor (ROE, stability, leverage)
- [[entities/dividend-yield-factor]] — Dividend Yield faktor

### Mérőszámok
- [[entities/alpha]] — Jensen's Alpha (faktor regresszió intercept)
- [[entities/beta]] — Piaci béta (szisztematikus kockázat)
- [[entities/sharpe-ratio]] — Kockázattal korrigált hozam + Deflated SR
- [[entities/information-ratio]] — Aktív hozam / tracking error + Fundamental Law

### Adatforrások
- [[entities/ken-french-data-library]] — FF faktor hozamok, portfólió adatok (1926–present)
- [[entities/gdelt]] — GDELT Event DB + GKG: geopolitikai és sentiment adatforrás

## Concepts
_Absztrakt fogalmak amik entitásokon átívelnek._

- [[concepts/value-premium]] — Value részvények szisztematikus felülteljesítése
- [[concepts/factor-zoo]] — 316+ faktor, data mining probléma
- [[concepts/multiple-testing]] — Többszörös tesztelés: FWER, FDR, t > 3.0 küszöb
- [[concepts/factor-cyclicality]] — Faktorok ciklikus alul/felülteljesítése
- [[concepts/covariance-matrix]] — Kovariancia mátrix és faktor dekompozíció
- [[concepts/news-sentiment-factor]] — Hírek/média sentiment mint faktor (GDELT, FinBERT, NLP)

## Methodology
_Standard eljárások lépésről lépésre._

- [[methodology/factor-validation]] — Faktor validációs eljárás (t > 3.0, OOS, robusztusság, DSR/PBO)
- [[methodology/deflated-sharpe-ratio]] — Deflated Sharpe Ratio: backtest overfitting korrekció
- [[methodology/backtest-overfitting-detection]] — PBO/CSCV + DSR + MinBTL eszköztár
- [[methodology/backtesting]] — Backteszt végrehajtási útmutató (buktatók, pipeline)
- [[methodology/cross-validation]] — Cross-validation pénzügyi idősorokra (k-fold, rolling, CSCV)

## Source Summaries
_Feldolgozott források kivonatai._

### Alapkövek
- [[source_summaries/markowitz-1952]] — Markowitz (1952): Portfolio Selection (MPT)
- [[source_summaries/sharpe-1964]] — Sharpe (1964): Capital Asset Prices (CAPM)
- [[source_summaries/fama-french-1993]] — Fama & French (1993): Common Risk Factors (FF3)
- [[source_summaries/carhart-1997]] — Carhart (1997): Mutual Fund Persistence (4F)
- [[source_summaries/fama-french-2014]] — Fama & French (2014): Five-Factor Model (FF5)

### Statisztikai kritika & módszertan
- [[source_summaries/harvey-liu-zhu-2016]] — Harvey, Liu & Zhu (2016): factor zoo, t > 3.0
- [[source_summaries/bailey-lopez-de-prado-2014-dsr]] — Bailey & López de Prado (2014): Deflated Sharpe Ratio
- [[source_summaries/bailey-borwein-lopez-de-prado-zhu-2015-pbo]] — Bailey et al. (2015): Probability of Backtest Overfitting
- [[source_summaries/simonian-2024-model-validation]] — Simonian (2024): Investment Model Validation (CFA)

### Factor investing & ipari alkalmazás
- [[source_summaries/msci-foundations-2013]] — MSCI: Foundations of Factor Investing
- [[source_summaries/kruger-2007]] — Kruger (2007): Mutual Fund Persistence (holdings)
- [[source_summaries/bender-nielsen-2010]] — Bender & Nielsen (2010): Fundamental Factor Models
- [[source_summaries/barra-risk-model-handbook]] — Barra Risk Model Handbook
- [[source_summaries/barra-use4-2011]] — Barra USE4 Methodology Notes
- [[source_summaries/msci-facs-2018]] — MSCI FaCS White Paper
- [[source_summaries/msci-factor-indexes-2018]] — MSCI Barra Factor Indexes Methodology
- [[source_summaries/msci-facs-esg-2018]] — MSCI FaCS + ESG Methodology

### KKE & Emerging Markets
- [[source_summaries/claesson-2021]] — Claesson (2021): FF models in Emerging Markets (26 ország)
- [[source_summaries/foye-mramor-pahor-2016]] — Foye, Mramor & Pahor (2016): FF3 a KKE EU-ban

### GDELT & News Sentiment
- [[source_summaries/shen-xia-shuai-gao-2022]] — Shen et al. (2022): GDELT GKG sentiment kínai piacokon
- [[source_summaries/zhang-2025]] — Zhang (2025): GDELT + FinBERT + XGBoost macro alpha
- [[source_summaries/consoli-pezzoli-tosetti-2020]] — Consoli et al. (2020): GDELT olasz államkötvény spread

## Comparisons
_Összevetések._

- [[comparisons/barra-vs-fama-french]] — Barra vs Fama-French: módszertan, cél, felhasználás
- [[comparisons/ff3-vs-ff5]] — FF3 vs Carhart 4F vs FF5: melyiket mikor
- [[comparisons/capm-vs-multifactor]] — CAPM vs Multi-Factor modellek evolúciója

## Open Questions
_Amit nem tudunk, amit tesztelni kell._

- [[open_questions/hml-redundancy]] — HML redundáns az FF5-ben? (contested)
- [[open_questions/kke-factor-premiums]] — Működnek-e az FF faktorok a KKE régióban?
- [[open_questions/missing-sources]] — Hiányzó alapforrások listája

---

_Ez az index automatikusan frissül minden ingest és lint művelet során._
