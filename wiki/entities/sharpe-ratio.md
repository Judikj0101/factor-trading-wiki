---
type: entity
tags: [performance, risk-management, portfolio]
confidence: high
last_reviewed: 2026-04-14
related: [[entities/alpha]], [[entities/beta]], [[entities/information-ratio]]
---

# Sharpe Ratio

## Definíció

A kockázattal korrigált hozam leggyakoribb mérőszáma (Sharpe 1966). Az egységnyi teljes kockázatra (volatilitás) jutó többlethozam.

$$SR = \frac{E(R_p) - R_F}{\sigma_p}$$

Ahol:
- $E(R_p)$: a portfólió várható hozama
- $R_F$: kockázatmentes ráta
- $\sigma_p$: a portfólió hozamának standard deviációja

## Értelmezés

| SR érték | Értékelés |
|---|---|
| < 0 | A kockázatmentes rátánál rosszabb |
| 0 – 0.5 | Gyenge |
| 0.5 – 1.0 | Elfogadható |
| 1.0 – 2.0 | Jó |
| > 2.0 | Kiváló (ritkán fenntartható hosszú távon) |

## Gyakorlati megjegyzések

- **Éves vs havi:** havi SR-t $\sqrt{12}$-vel szorozva kapjuk az évesítettet (feltéve i.i.d. hozamokat)
- **Nem normális eloszlás:** ha a hozamok fat-tailed vagy skewed, a SR félrevezető lehet → kiegészítő mérőszámok: Sortino ratio (downside deviation), Calmar ratio (max drawdown)
- **Faktorok Sharpe rátái:** a momentum faktornak jellemzően a legmagasabb a SR, de a momentum crash-ek (tail risk) nem tükröződnek a SR-ban
- **Overfitting:** backtesztben könnyű magas SR-t mutatni — Harvey et al. (2016) figyelmeztetései érvényesek

## Deflated Sharpe Ratio (DSR)

A Sharpe ratio inflalodhat multiple testing es nem-normalis eloszlas miatt. A [[methodology/deflated-sharpe-ratio|Deflated Sharpe Ratio]] (Bailey & Lopez de Prado 2014) korrigalja mindket hatast. Ld. reszletesen: [[source_summaries/bailey-lopez-de-prado-2014-dsr]].

## Kapcsolódó mérőszámok

- [[entities/information-ratio]]: a tracking error-re normált aktív hozam
- Sortino ratio: $SR_{down} = (R_p - R_F) / \sigma_{down}$
- Calmar ratio: annualized return / max drawdown

## Források

- Sharpe (1966): "Mutual Fund Performance"
- [[source_summaries/bailey-lopez-de-prado-2014-dsr|Bailey & Lopez de Prado (2014)]]: Deflated Sharpe Ratio
- [[source_summaries/simonian-2024-model-validation|Simonian (2024)]]: Investment Model Validation
