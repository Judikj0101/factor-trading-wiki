---
type: entity
tags: [performance, risk-management, portfolio]
confidence: high
last_reviewed: 2026-04-14
related: [[entities/sharpe-ratio]], [[entities/alpha]], [[entities/barra-risk-model]]
---

# Information Ratio (IR) & Tracking Error

## Information Ratio

Az aktív hozam és az aktív kockázat (tracking error) aránya. Az aktív management "hatékonyságának" mérőszáma.

$$IR = \frac{R_p - R_b}{\sigma(R_p - R_b)} = \frac{\text{Active Return}}{\text{Tracking Error}}$$

Ahol:
- $R_p - R_b$: aktív hozam (portfólió − benchmark)
- $\sigma(R_p - R_b)$: tracking error

## Tracking Error

A portfólió és a benchmark hozamkülönbségének standard deviációja. Az "aktív kockázat" mérőszáma.

$$TE = \sigma(R_p - R_b)$$

## Értelmezés

| IR érték | Értékelés |
|---|---|
| < 0 | Benchmark alatti teljesítmény |
| 0 – 0.5 | Gyenge aktív management |
| 0.5 – 1.0 | Jó aktív management |
| > 1.0 | Kiváló (ritka, nehezen fenntartható) |

## Kapcsolat a Sharpe ratio-val

- **Sharpe ratio:** teljes hozam / teljes kockázat (a kockázatmentes rátához képest)
- **Information ratio:** aktív hozam / aktív kockázat (a benchmarkhoz képest)
- Ha a benchmark a kockázatmentes ráta, a kettő megegyezik

## Grinold & Kahn: Fundamental Law of Active Management

$$IR \approx IC \cdot \sqrt{BR}$$

Ahol:
- $IC$: Information Coefficient — a menedzser előrejelző képessége (korreláció a forecast és a realized return között)
- $BR$: Breadth — az independent bets száma évente

Ez a formula a Barra/Grinold-Kahn keretrendszer központi eredménye: a jó aktív management = jó előrejelzés × sok független döntés.

## Források

- [[source_summaries/barra-risk-model-handbook]]
- Grinold & Kahn: *Active Portfolio Management* (1995, 2000)
