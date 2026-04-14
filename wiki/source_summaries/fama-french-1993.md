---
type: source_summary
tags: [factor-model, cross-section, regression, size, value]
confidence: high
last_reviewed: 2026-04-14
related: [[entities/fama-french-five-factor-model]], [[entities/smb]], [[entities/hml]], [[entities/market-risk-premium]], [[entities/alpha]], [[comparisons/ff3-vs-ff5]]
---

# Fama & French (1993) — Common Risk Factors in the Returns on Stocks and Bonds

**Szerzők:** Eugene F. Fama, Kenneth R. French
**Megjelenés:** 1993, Journal of Financial Economics, 33, 3–56
**Raw forrás:** `raw/papers/Fama-French_JFE93.md`

## Fő állítások

1. **Öt közös kockázati faktor** azonosítható a részvény- és kötvényhozamokban:
   - **3 részvénypiaci faktor:** market, size (SMB), book-to-market (HML)
   - **2 kötvénypiaci faktor:** TERM (kamatláb kockázat), DEF (default kockázat)

2. A size és book-to-market faktorok **erős közös varianciát** ragadnak meg a részvényhozamokban — ez bizonyíték arra, hogy szisztematikus kockázati tényezők.

3. A háromfaktoros modell intercept-jei ($\alpha_i$) közel nullák a 25 size × B/M portfólióra → a modell jól magyarázza a cross-section hozamokat.

4. A részvény- és kötvénypiac **nem szegmentált:** a term-structure faktorok megjelennek a részvényhozamokban is, de a stock-market faktorok felszívják ezt a hatást.

## A háromfaktoros modell (FF3)

$$R_{it} - R_{Ft} = \alpha_i + b_i(R_{Mt} - R_{Ft}) + s_i \cdot SMB_t + h_i \cdot HML_t + e_{it}$$

## Faktor konstrukció

### SMB (Small Minus Big)
- NYSE median market cap alapján Size sort
- 2×3 sort: Size × B/M (independent)
- $SMB = \frac{1}{3}(SL + SM + SH) - \frac{1}{3}(BL + BM + BH)$

### HML (High Minus Low)
- NYSE breakpoints: 30. és 70. percentilis B/M
- $HML = \frac{1}{2}(SH + BH) - \frac{1}{2}(SL + BL)$

### Kötvénypiaci faktorok
- **TERM:** long-term government bond return − 1-month T-bill rate (kamatláb kockázat)
- **DEF:** long-term corporate bond portfolio return − long-term government bond return (default kockázat)

## Empirikus motiváció (Fama & French 1992a alapján)

- A piaci beta ($\beta$) önmagában **nem magyarázza** a cross-section hozamokat
- Size és B/M **jól magyarázza** — de ezek "ad hoc" változók
- A paper célja: megmutatni, hogy size és B/M szisztematikus kockázati faktorok proxyjai (nem anomáliák)
- A distress risk hipotézis: magas B/M cégek pénzügyi nehézséggel küzdenek → magasabb kockázat → magasabb hozam

## Fő eredmények részletesen

- A 25 size × B/M portfólió $R^2$ értékei a háromfaktoros regresszióban: **tipikusan 0.93–0.97**
- Az intercept-ek ($\alpha$) statisztikailag nem szignifikánsak a legtöbb portfólióra
- Az SMB és HML faktorok hozzáadása **drámaian javítja** a magyarázó erőt a CAPM-hez képest
- A market faktor egyedül ~70% $R^2$-t ad → SMB+HML hozzáadásával ~95%

## Limitációk

- Miért működik? A paper nem dönti el a risk vs mispricing vitát
- US-specifikus (NYSE, Amex, NASDAQ, 1963–1991)
- A size és B/M faktorok "ad hoc" jellege megmarad — nincs erős elméleti deriváció (ez motiválta az FF5-öt 2014-ben)

## Kapcsolódás a rendszerhez

Ez a paper az **alapító dokumentum** — a háromfaktoros modell és a modern factor investing innen indul. Az FF5 (2014) ennek a bővítése, az MSCI factor indexek pedig erre és a Barra modellre épülnek.

## Kapcsolódó források

- [[source_summaries/fama-french-2014]] — az FF5 bővítés
- [[source_summaries/kruger-2007]] — mutual fund alpha mérés FF3/Carhart modellel
