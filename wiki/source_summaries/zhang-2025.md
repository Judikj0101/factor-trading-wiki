---
type: source_summary
tags: [sentiment, gdelt, machine-learning, time-series, fx, fixed-income]
confidence: medium
last_reviewed: 2026-04-14
related: [[entities/gdelt]], [[concepts/news-sentiment-factor]], [[concepts/factor-zoo]]
---

# Zhang (2025) — Interpretable Machine Learning for Macro Alpha: A News Sentiment Case Study

## Bibliografia

- **Szerzo:** Yuke Zhang
- **Ev:** 2025
- **Forras:** arXiv:2505.16136v1
- **GitHub:** https://github.com/yukepenn/macro-news-sentiment-trading
- **Forras fajl:** `raw/papers/2505.16136v1.md`

## Fo allitasok

1. A **GDELT v2 API** es **FinBERT** (finance-domain BERT) kombinaciojaval epített napi sentiment indexek szignifikans **makro alpha-t** generalnak FX es kotvenypiacon.
2. **XGBoost** klasszifikator **masnapra jelzi eloer a hozamirany** EUR/USD, USD/JPY es 10 eves US Treasury futures (ZN) piacokon.
3. **Out-of-sample teljesitmeny** (2017–2025, expanding window):
   - EUR/USD: Sharpe 5.87, CAGR > 50%
   - USD/JPY: Sharpe 4.65, CAGR > 50%
   - ZN (Treasury): Sharpe 4.65, CAGR > 22%
4. **SHAP elemzes** megerositi: a **sentiment dispersion** es **article impact** a legfontosabb prediktiv feature-ok.
5. A logisztikus regresszio (baseline) is szignifikans, de az XGBoost jelentosen felulmúlja.

## Modszertan

- **Adatgyujtes:** GDELT v2, 2015. januar – 2025. aprilis, EventCode 100–199 (gazdasagi/diplomaciai esemenyek), napi top 100 cikk.
- **Sentiment scoring:** FinBERT (ProsusAI/finbert), polarity score: $s_{i,t} = P_{Pos} - P_{Neg} \in [-1, +1]$.
- **Feature engineering:** Mean Sentiment, Dispersion, News Volume, Article Impact, Goldstein Score, + lagged (1–3 nap) es moving average (5, 20 nap) valtozatok.
- **Modell:** XGBoost klasszifikator, 5-fold expanding-window CV.
- **Tranzakcios koltsegek:** figyelembe veve a backtesztben.

## Relevans eredmenyek a factor trading rendszerhez

- **Kivételesen magas Sharpe-ok** — a szerzok maguk is elismerik, hogy ezek rendkivul magasak, ami overfitting kockazatot jelezhet.
- **GDELT + FinBERT pipeline** reprodukalható es nyilt forrasu — a MMCP projektben is alkalmazható megkozelites.
- **Sentiment dispersion** mint legfontosabb feature — osszevag a Shen et al. (2022) tone dispersion eredmenyeivel.
- **Macro (FX, fixed income) fókusz** — nem equity, hanem makro asset class-okban.
- A **Goldstein skala** hasznos feature — ez releváns az MMCP geopolitikai kontextusában.

## Limitaciok

- A Sharpe ratok **gyanúsan magasak** (5.87) — overfitting kockazat meg expanding window-val is.
- Nincs live trading eredmeny — csak backtest.
- A FinBERT headline-okra alkalmazva — a cimbol szarmazo sentiment torzithat.
- A GDELT EventCode 100–199 szurese szubjektiv — mas szuresek mas eredmenyt adhatnanak.
- **Replikáció szükseges** — a GitHub repo elerheto, ami pozitiv.
