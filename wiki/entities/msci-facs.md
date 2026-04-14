---
type: entity
tags: [factor-model, classification, factor-investing]
confidence: high
last_reviewed: 2026-04-14
related: [[entities/barra-risk-model]], [[entities/fama-french-five-factor-model]], [[source_summaries/msci-facs-2018]], [[source_summaries/msci-factor-indexes-2018]]
---

# MSCI FaCS (Factor Classification Standard)

## Definíció

Az MSCI által 2018-ban bevezetett szabványos keretrendszer equity portfóliók faktor jellemzőinek elemzéséhez. A Barra GEMLT modell 16 style faktorát 8 faktor csoportba szervezi.

## A 8 faktor csoport

| Csoport | Tartalom | Risk premia? |
|---|---|---|
| **Value** | Book-to-Price, Earnings Yield | Igen |
| **Size** | Size, Size Nonlinearity | Igen |
| **Momentum** | Momentum, Short-term Reversal | Igen |
| **Volatility** | Beta, Residual Volatility | Igen (low vol prémium) |
| **Quality** | Profitability, Earnings Quality, Investment Quality, Leverage | Igen |
| **Yield** | Dividend Yield | Igen |
| **Growth** | Earnings Growth, Sales Growth | **Nem** |
| **Liquidity** | Trading Activity | **Nem** |

A Growth és Liquidity faktorok a kockázati modellben fontosak, de nem termelnek tartós prémiumot (lásd [[source_summaries/msci-foundations-2013]]).

## Alkalmazás

- Portfólió faktor profil elemzés és összehasonlítás
- Style drift monitoring
- Fund selection / due diligence
- Szabványos "közös nyelv" befektetők, alapkezelők és tanácsadók között

## Kapcsolat a wiki faktorokkal

| FaCS csoport | Wiki entity |
|---|---|
| Value | [[entities/hml]] |
| Size | [[entities/smb]] |
| Momentum | [[entities/momentum]] |
| Volatility | [[entities/low-volatility]] |
| Quality | [[entities/quality-factor]], [[entities/rmw]] |
| Yield | [[entities/dividend-yield-factor]] |

## Források

- [[source_summaries/msci-facs-2018]]
- [[source_summaries/msci-factor-indexes-2018]]
- [[source_summaries/msci-facs-esg-2018]]
