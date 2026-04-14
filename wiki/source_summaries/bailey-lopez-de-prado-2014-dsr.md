---
type: source_summary
tags: [statistics, backtesting, overfitting, performance]
confidence: high
last_reviewed: 2026-04-14
related: [[entities/sharpe-ratio]], [[concepts/multiple-testing]], [[concepts/factor-zoo]], [[methodology/factor-validation]], [[source_summaries/bailey-borwein-lopez-de-prado-zhu-2015-pbo]], [[methodology/deflated-sharpe-ratio]], [[methodology/backtest-overfitting-detection]]
---

# Bailey & Lopez de Prado (2014) — The Deflated Sharpe Ratio

**Szerzok:** David H. Bailey, Marcos Lopez de Prado
**Megjelenes:** 2014, Journal of Portfolio Management
**Raw forras:** `raw/papers/deflated-sharpe.md`

## Fo allitasok

1. **A Sharpe ratio inflalodik** ket forrasbol: (a) selection bias / multiple testing, (b) nem-normalis eloszlasu hozamok (skewness, kurtosis).
2. **Deflated Sharpe Ratio (DSR):** egy statisztikai teszt ami mindket inflaciot korrigalja. A DSR megadja annak valoszinuseget, hogy a valos SR meghalad egy kuruszobot, figyelembe veve a futtatott tesztek szamat es a hozamok eloszlasat.
3. **A holdout modszer nem ved meg** a backtest overfitting ellen, mert ignoralja a probalkozasok szamat (multiple testing).
4. **Memory effects** a penzugyi idosorokban: az overfittelest erdemes a legexlremebb mintazatokra, amiket a memory "undo-l" (visszafordit), igy az overfit strategiak out-of-sample veszteseget maximalizaljak.
5. **Optimal stopping (secretary problem):** a strategia konfiguraciok $1/e$ reszet (~37%) erdemes eloszor vegigprobalni, majd az elso olyat valasztani amelyik mindegyiket veri.

## A Deflated Sharpe Ratio formula

$$DSR = PSR(\hat{SR}_0) = Z\left[\frac{(\hat{SR} - \hat{SR}_0)\sqrt{T-1}}{\sqrt{1 - \hat{\gamma}_3 \hat{SR} + \frac{\hat{\gamma}_4 - 1}{4}\hat{SR}^2}}\right]$$

Ahol:

$$\hat{SR}_0 \approx \sqrt{V[\{SR_n\}]} \cdot \left((1-\gamma) \cdot Z^{-1}\left[1 - \frac{1}{N}\right] + \gamma \cdot Z^{-1}\left[1 - \frac{1}{N} \cdot e^{-1}\right]\right)$$

Valtozok:
- $\hat{SR}$: a kivalasztott strategia becsult Sharpe ratioja
- $\hat{SR}_0$: a varhatoertek-maximuma N fuggetlen probabol (rejection threshold)
- $T$: mintameret (pl. napi hozamok szama)
- $\hat{\gamma}_3$: a hozamok ferdesege (skewness)
- $\hat{\gamma}_4$: a hozamok csucssossaga (kurtosis)
- $V[\{SR_n\}]$: a tesztelt strategiak SR-jeinek varianciaja
- $N$: fuggetlen probalkozasok szama
- $\gamma \approx 0.5772$ (Euler-Mascheroni konstans)

## Numerikus pelda a paperbol

- Strategista: treasury seasonality, N=88 probalkovas, legjobb $\hat{SR} = 2.5$ (evesitett), T=1250 nap
- $\hat{\gamma}_3 = -3$, $\hat{\gamma}_4 = 10$, $V[\{SR_n\}] = 1$
- **Eredmeny: DSR = 0.90** → 90% valoszinuseg hogy a valos SR > 0 → a 95%-os kuuszob alatt, elutasitva!
- Ha csak N=46 probaval talalta volna → DSR = 0.9505 → elfogadhato
- Ha normalis eloszlasu hozamok ($\hat{\gamma}_3=0, \hat{\gamma}_4=3$) → DSR elfogadhato N=88 mellett is

## Kulcs osszefuggesek

| Felfujosag forrasa | Hatas | DSR korrekcioja |
|---|---|---|
| Multiple testing (N no) | Varhatoertek max SR no | $\hat{SR}_0$ emelkedik |
| Negativ skewness | SR tulon mert | Nevezo csokkent |
| Excess kurtosis | SR tulon mert | Nevezo csokkent |
| Rovid minta (T kicsi) | Bizonytalan becsles | Nevezo no |

## Kapcsolodas Harvey et al. (2016) keretrendszerhez

A DSR es Harvey & Liu (2014) komplementerek:
- Harvey & Liu: Benjamini-Hochberg alapu threshold uj faktoroknak
- DSR: Extreme Value Theory alapu threshold + non-normalitas korrekcioja
- Mindketto alkalmazhato egymasra is

## Limitaciok

- Feltetelezi hogy a probalkozasok SR-jei normalis eloszlasuak (a hozamok nem feltetlenul)
- A fuggetlen probalkozasok szamanak ($N$) meghatarozasa szubjektiv (Appendix 3 ad utmutatot korrelalt esetre)
- Nem kezeli a regime change / strukturalis tores problemajat — a memory effects targyalas ezt csak reszlegesen fedi

## Kapcsolodas a rendszerhez

A DSR a [[methodology/factor-validation]] masodik szuroje: miutan a t > 3.0 szurot (Harvey et al. 2016) alkalmaztuk, a DSR megmutatja, hogy az adott strategia SR-je a probalkozasok szamat is figyelembe veve szignifikans-e. Kulonosen fontos [[entities/sharpe-ratio]] ertelmezesenel es barmilyen backteszt eredmeny biralatnal.
