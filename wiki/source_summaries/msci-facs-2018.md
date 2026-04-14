---
type: source_summary
tags: [factor-model, factor-investing, classification]
confidence: high
last_reviewed: 2026-04-14
related: [[entities/msci-facs]], [[entities/barra-risk-model]], [[source_summaries/msci-foundations-2013]]
---

# MSCI (2018) — Introducing MSCI FaCS

**Szerzők:** George Bonne, Leon Roisenberg, Raman Aylur Subramanian, Dimitris Melas
**Megjelenés:** January 2018
**Raw forrás:** `raw/standards/Introducing-MSCI-FaCS-White-Paper.md`

## Fő tartalom

A MSCI FaCS (Factor Classification Standard) bevezetése — egy szabványos keretrendszer equity portfóliók faktor jellemzőinek elemzéséhez és riportolásához.

## FaCS struktúra

A Barra GEMLT modell 16 style faktorát **8 faktor csoportba** szervezi:

| Faktor csoport | Alkotó Barra faktorok |
|---|---|
| **Value** | Book-to-Price, Earnings Yield, stb. |
| **Size** | Size, Size Nonlinearity |
| **Momentum** | Momentum, Short-term Reversal |
| **Volatility** | Beta, Residual Volatility |
| **Quality** | Profitability, Earnings Quality, Investment Quality, Leverage |
| **Yield** | Dividend Yield |
| **Growth** | Earnings Growth, Sales Growth |
| **Liquidity** | Trading Activity |

## Alkalmazások

1. **Fund reporting:** portfólió faktor profil vizualizáció
2. **Fund comparison:** különböző alapok faktor exposure összevetése
3. **Style drift assessment:** az alap faktor exposure-jának időbeli változása

## Fő eredmények

- 3000+ aktívan kezelt US és globális alap elemzése
- A legtöbb alap exposure-ja megfelel a nevének, de **vannak eltérések**
- A FaCS standardizálja a faktor nyelvet az iparágban

## Kapcsolódás a rendszerhez

A FaCS jó keretrendszer bármilyen portfólió vagy stratégia faktor profiljának értékeléséhez. A 8 faktor csoport egy használható taxonómia.

## Limitációk

- A Barra GEMLT modellre épül → proprietáris
- Nem tartalmaz risk premia/alpha különbséget (a Growth és Liquidity is benne van, holott ezek nem risk premia faktorok)
