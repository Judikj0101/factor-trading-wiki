---
type: comparison
tags: [factor-model, capm, cross-section]
confidence: high
last_reviewed: 2026-04-14
related: [[entities/capm]], [[entities/fama-french-five-factor-model]], [[entities/barra-risk-model]]
---

# CAPM vs Multi-Factor modellek

## Az evolúció

```
CAPM (1964)          → egyetlen faktor (market)
 ↓ anomáliák
FF3 (1993)           → 3 faktor (market + size + value)
 ↓ momentum
Carhart 4F (1997)    → 4 faktor (+ momentum)
 ↓ profitability, investment
FF5 (2014)           → 5 faktor (+ RMW + CMA, − MOM)
 ↓ ipari alkalmazás
Barra (USE4, GEM2)   → 60+ faktor (industry + style + country)
```

## Összehasonlítás

| Dimenzió | CAPM | Multi-Factor (FF5/Barra) |
|---|---|---|
| **Faktorok** | 1 (market) | 5–60+ |
| **Feltevések** | Erős (homogén várakozások, stb.) | Gyengébb (empirikus) |
| **Cross-section magyarázó erő** | Gyenge (~70% anomália megmagyarázatlan) | Erős (FF5: 71–94%) |
| **Egyszerűség** | Nagyon egyszerű | Komplexebb |
| **Kockázat definíció** | Béta = az egyetlen releváns kockázat | Több dimenzió: size, value, profitability, stb. |
| **Anomáliák** | Nem képes magyarázni (size, value, momentum) | Nagyrészt megmagyarázza |

## Miért nem elég a CAPM

A CAPM egy elegáns elméleti keret, de empirikusan **megbukott**:

1. **Size effect:** kis cégek felülteljesítenek a bétájuk által implikáltnál
2. **Value effect:** magas B/M részvények felülteljesítenek
3. **Low beta anomaly:** alacsony béta részvények kockázattal korrigálva jobbak
4. **Momentum:** a CAPM-ből semmilyen módon nem következik

A multi-factor modellek ezeket az anomáliákat **szisztematikus kockázati faktorokként** kezelik.

## A CAPM továbbél

A CAPM annak ellenére, hogy empirikusan bukott, továbbra is alapvető:
- **Oktatásban:** az első modell amit tanítanak
- **WACC számításban:** a tőkeköltség becslésénél a béta ma is standard
- **Gondolkodási keretként:** a market faktor minden multi-factor modellben benne van
- **Benchmarkként:** a CAPM alpha a legegyszerűbb excess return mérce

## Források

- [[source_summaries/msci-foundations-2013]]
- [[source_summaries/fama-french-2014]]
- [[source_summaries/barra-use4-2011]]
