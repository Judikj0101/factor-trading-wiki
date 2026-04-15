---
type: log
---

# Factor Trading Wiki — Log

Kronologikus napló minden wiki műveletről. Append-only — korábbi bejegyzések nem törölhetők.

---

## [2026-04-14] init | Wiki létrehozva
- Schema: CLAUDE.md v1
- Struktúra: raw/{papers,datasets,standards,code}, wiki/{entities,concepts,methodology,source_summaries,comparisons,open_questions}
- Speciális fájlok: index.md, log.md, contradictions.md
- Állapot: üres vault, kész az első ingest-re

## [2026-04-14] ingest | Fama & French (2014) — A Five-Factor Asset Pricing Model
- Source summary: [[source_summaries/fama-french-2014]]
- Új oldalak: [[entities/fama-french-five-factor-model]], [[entities/market-risk-premium]], [[entities/smb]], [[entities/hml]], [[entities/rmw]], [[entities/cma]], [[concepts/value-premium]], [[open_questions/hml-redundancy]]
- Frissített oldalak: —
- Ellentmondások: nem

## [2026-04-14] ingest | Harvey, Liu & Zhu (2016) — ...and the Cross-Section of Expected Returns
- Source summary: [[source_summaries/harvey-liu-zhu-2016]]
- Új oldalak: [[concepts/factor-zoo]], [[concepts/multiple-testing]], [[methodology/factor-validation]]
- Frissített oldalak: —
- Ellentmondások: nem

## [2026-04-14] ingest | MSCI (2013) — Foundations of Factor Investing
- Source summary: [[source_summaries/msci-foundations-2013]]
- Új oldalak: [[entities/momentum]], [[entities/low-volatility]], [[entities/quality-factor]], [[entities/dividend-yield-factor]], [[concepts/factor-cyclicality]]
- Frissített oldalak: —
- Ellentmondások: nem

## [2026-04-14] ingest | Barra Risk Model Handbook (2007) + USE4 Methodology (2011)
- Source summaries: [[source_summaries/barra-risk-model-handbook]], [[source_summaries/barra-use4-2011]]
- Új oldalak: [[entities/barra-risk-model]], [[concepts/covariance-matrix]]
- Ellentmondások: nem

## [2026-04-14] ingest | Kruger (2007) — Persistence in Mutual Fund Performance
- Source summary: [[source_summaries/kruger-2007]]
- Ellentmondások: nem

## [2026-04-14] ingest | Bender & Nielsen (2010) — Fundamentals of Fundamental Factor Models
- Source summary: [[source_summaries/bender-nielsen-2010]]
- Ellentmondások: nem

## [2026-04-14] ingest | MSCI FaCS + Factor Indexes + ESG Methodology (2018)
- Source summaries: [[source_summaries/msci-facs-2018]], [[source_summaries/msci-factor-indexes-2018]], [[source_summaries/msci-facs-esg-2018]]
- Új oldalak: [[entities/msci-facs]]
- Ellentmondások: nem

## [2026-04-14] sort | raw/raw inbox szétválogatása
- papers/ (5): Fama-French 2014, Foundations, Mutual Fund Persistence, Harvey-Liu-Zhu, SSRN-1707661
- standards/ (5): MSCI FaCS, Factor Indexes, USE4, Barra Handbook, FaCS+ESG
- PDF→MD extrakció: PyPDF2, eredeti PDF-ek megtartva

## [2026-04-14] expand | Hiányzó entity-k, comparison-ok, forráslista
- Új entity oldalak: [[entities/capm]], [[entities/carhart-four-factor-model]], [[entities/alpha]], [[entities/beta]], [[entities/sharpe-ratio]], [[entities/information-ratio]]
- Új comparison oldalak: [[comparisons/barra-vs-fama-french]], [[comparisons/ff3-vs-ff5]], [[comparisons/capm-vs-multifactor]]
- Új open question: [[open_questions/missing-sources]] — hiányzó alapforrások priorizált listája
- Ellentmondások: nem

## [2026-04-14] ingest | Fama & French (1993) — Common Risk Factors in the Returns on Stocks and Bonds
- Source summary: [[source_summaries/fama-french-1993]]
- Frissített oldalak: [[entities/smb]] (eredeti konstrukció hozzáadva), [[entities/hml]] (eredeti konstrukció), [[entities/fama-french-five-factor-model]] (előzmények linkek)
- Ellentmondások: nem
- Megjegyzés: az FF3 alapító paper — a wiki hivatkozási hálózat legfontosabb hiányát pótolja

## [2026-04-14] ingest | Carhart (1997) — On Persistence in Mutual Fund Performance
- Source summary: [[source_summaries/carhart-1997]]
- Frissített oldalak: [[entities/carhart-four-factor-model]], [[entities/momentum]]
- Ellentmondások: nem
- Megjegyzés: JSTOR verzió beszerzve (szöveg kinyerhető), source summary frissítve részletes eredményekkel

## [2026-04-14] note | Fama-French_JFE93 (1).pdf = duplikátum
- A letöltött fájl az FF 1993 paper másolata, nem az FF 1992 ("The Cross-Section of Expected Stock Returns")
- Az FF 1992 továbbra is hiányzik — lásd [[open_questions/missing-sources]]

## [2026-04-14] ingest | Sharpe (1964) — Capital Asset Prices (CAPM)
- Source summary: [[source_summaries/sharpe-1964]]
- Frissített oldalak: [[entities/capm]] (forrás hivatkozások)
- Ellentmondások: nem

## [2026-04-14] ingest | Markowitz (1952) — Portfolio Selection
- Source summary: [[source_summaries/markowitz-1952]]
- Megjegyzés: scanned PDF, source summary saját tudás alapján

## [2026-04-14] ingest | Ken French Data Library
- Új entity: [[entities/ken-french-data-library]]
- Forrás: https://mba.tuck.dartmouth.edu/pages/faculty/ken.french/data_library.html

## [2026-04-14] ingest | Methodology források (3 db)
- Source summaries: [[source_summaries/bailey-lopez-de-prado-2014-dsr]], [[source_summaries/bailey-borwein-lopez-de-prado-zhu-2015-pbo]], [[source_summaries/simonian-2024-model-validation]]
- Új methodology oldalak: [[methodology/deflated-sharpe-ratio]], [[methodology/backtest-overfitting-detection]], [[methodology/backtesting]], [[methodology/cross-validation]]
- Frissített oldalak: [[entities/sharpe-ratio]], [[methodology/factor-validation]], [[concepts/multiple-testing]], [[concepts/factor-zoo]]
- Ellentmondások: nem

## [2026-04-14] ingest | KKE & Emerging Markets (2 forrás)
- Source summaries: [[source_summaries/claesson-2021]], [[source_summaries/foye-mramor-pahor-2016]]
- Új open question: [[open_questions/kke-factor-premiums]]
- Ellentmondások: nem

## [2026-04-14] ingest | GDELT & News Sentiment (3 forrás)
- Source summaries: [[source_summaries/shen-xia-shuai-gao-2022]], [[source_summaries/zhang-2025]], [[source_summaries/consoli-pezzoli-tosetti-2020]]
- Új entity: [[entities/gdelt]]
- Új concept: [[concepts/news-sentiment-factor]]
- Ellentmondások: nem

## [2026-04-15] ingest | Monetáris politika & EMDE spillover (3 forrás)
- Source summaries: [[source_summaries/dinerstein-yannelis-chen-2023]], [[source_summaries/adrian-gelos-lamersdorf-moench-2024]], [[source_summaries/arteta-kamin-ruch-2022]]
- Új entity oldalak: [[entities/term-premium]]
- Új concept oldalak: [[concepts/monetary-policy-spillover]]
- Frissített oldalak: [[open_questions/kke-factor-premiums]] (US monetáris sokktípus csatorna hozzáadva), [[wiki/index]] (új szekciók)
- Ellentmondások: nem
- Megjegyzés: w31247 (Dinerstein et al.) közvetlen relevancia alacsony — US fogyasztói pénzügyek; work1195 (Adrian et al.) és IDU (Arteta et al.) erősen releváns a KKE makro faktor kutatáshoz

## [2026-04-15] ingest | 2. batch — 8 forrás (alapkövek + rezsim + decay)
- Source summaries: [[source_summaries/fama-french-1992]], [[source_summaries/fama-macbeth-1973]], [[source_summaries/ross-1976]], [[source_summaries/novy-marx-2013]], [[source_summaries/caldara-iacoviello-2018]], [[source_summaries/mclean-pontiff-2015]], [[source_summaries/ang-bekaert-2002]], [[source_summaries/shanken-zhou-2006]]
- Új entity oldalak: [[entities/gpr-index]], [[entities/apt]]
- Új concept oldalak: [[concepts/rezsimdetekcio]], [[concepts/faktor-decay]]
- Új methodology oldalak: [[methodology/fama-macbeth-regresszio]]
- Frissített oldalak: [[entities/rmw]] (Novy-Marx link), [[entities/gdelt]] (GPR cross-ref), [[concepts/factor-zoo]] (decay szekció), [[concepts/multiple-testing]] (decay link), [[open_questions/missing-sources]] (8 forrás lezárva)
- Ellentmondások: nem
- Megjegyzés: Fama-MacBeth.pdf és FF1992 scanned — source summary saját tudás alapján
