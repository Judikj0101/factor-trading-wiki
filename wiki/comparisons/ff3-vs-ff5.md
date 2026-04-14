---
type: comparison
tags: [factor-model, cross-section]
confidence: high
last_reviewed: 2026-04-14
related: [[entities/fama-french-five-factor-model]], [[entities/carhart-four-factor-model]], [[entities/capm]], [[entities/hml]], [[entities/rmw]], [[entities/cma]]
---

# FF3 vs Carhart 4F vs FF5: melyiket mikor

## A három modell

| | FF3 (1993) | Carhart 4F (1997) | FF5 (2014) |
|---|---|---|---|
| Market | $\checkmark$ | $\checkmark$ | $\checkmark$ |
| SMB | $\checkmark$ | $\checkmark$ | $\checkmark$ |
| HML | $\checkmark$ | $\checkmark$ | $\checkmark$ |
| MOM | | $\checkmark$ | |
| RMW | | | $\checkmark$ |
| CMA | | | $\checkmark$ |
| **Faktorok** | **3** | **4** | **5** |

## Miben különböznek

### FF3 → FF5: profitability és investment hozzáadása
- Az FF3 value faktorát (HML) az RMW és CMA együtt képes megmagyarázni → [[open_questions/hml-redundancy]]
- Az FF5 jobban magyarázza a cross-section hozam variációt (71–94% vs alacsonyabb)
- De az FF5 **nem tartalmaz momentumot**

### FF3 → Carhart: momentum hozzáadása
- A momentum az egyik legerősebb anomália, de Fama & French nem tekintik kockázati faktornak
- A Carhart modell a mutual fund evaluation standardja

### Carhart vs FF5: momentum vs profitability/investment
- A Carhart modell a **hozam perzisztencia** magyarázatára optimális
- Az FF5 az **asset pricing** tesztelésre optimális
- Informálisan: FF5 + MOM = "FF6" is használható

## Mikor melyiket

| Feladat | Modell |
|---|---|
| Egyszerű akadémiai teszt | FF3 |
| Mutual fund alpha / manager evaluation | Carhart 4F |
| Asset pricing, faktor tesztelés | FF5 |
| Legteljesebb lefedettség | FF5 + MOM ("FF6") |
| Historikus összehasonlíthatóság (régi irodalommal) | FF3 |

## Gyakorlati tanács

Ha **egy modellt** kell választani, az FF5 + MOM a legátfogóbb. De a modell választás a kérdéstől függ — nem attól, hogy melyik "jobb".

## Források

- [[source_summaries/fama-french-2014]]
- [[source_summaries/kruger-2007]]
