---
type: entity
tags: [factor-model, cross-section, regression]
confidence: high
last_reviewed: 2026-04-14
related: [[entities/smb]], [[entities/hml]], [[entities/rmw]], [[entities/cma]], [[entities/market-risk-premium]], [[concepts/value-premium]], [[source_summaries/fama-french-2014]]
---

# Fama-French Five-Factor Model

## Definíció

A Fama és French (2014) által javasolt asset pricing modell, amely öt szisztematikus kockázati faktorral magyarázza a részvényhozamok cross-section variációját:

$$R_{it} - R_{Ft} = a_i + b_i(R_{Mt} - R_{Ft}) + s_i \cdot SMB_t + h_i \cdot HML_t + r_i \cdot RMW_t + c_i \cdot CMA_t + e_{it}$$

| Faktor | Leírás |
|--------|--------|
| [[entities/market-risk-premium\|$R_M - R_F$]] | Piaci kockázati prémium |
| [[entities/smb\|SMB]] | Size faktor (Small Minus Big) |
| [[entities/hml\|HML]] | Value faktor (High Minus Low B/M) |
| [[entities/rmw\|RMW]] | Profitability faktor (Robust Minus Weak) |
| [[entities/cma\|CMA]] | Investment faktor (Conservative Minus Aggressive) |

## Előzmények

- [[entities/capm|CAPM]] (Sharpe 1964, Lintner 1965): 1 faktor (market)
- **Fama-French 3-factor (1993):** Market + SMB + HML — [[source_summaries/fama-french-1993]]
- [[entities/carhart-four-factor-model|Carhart 4-factor]] (1997): FF3 + Momentum (nem része az FF5-nek)
- **Fama-French 5-factor (2014): Market + SMB + HML + RMW + CMA**

## Elméleti motiváció

A dividend discount model / clean surplus accounting alapján a B/M ráta, a várható profitabilitás és a várható beruházás együttesen meghatározzák az elvárt hozamot. A profitability és investment faktorok hozzáadása ezt az elméleti struktúrát tükrözi.

## Fő eredmények

- Az ötfaktoros modell 71–94%-át magyarázza a cross-section hozamvarianciának (size, B/M, OP, Inv portfóliók).
- A GRS teszt formálisan elutasítja a modellt, de ez normális nagy mintáknál.
- A HML potenciálisan redundáns — lásd [[open_questions/hml-redundancy]].

## Limitációk

- Nem tartalmaz momentum faktort.
- A GRS teszt elutasítja — tehát nem teljes modell.
- Problémás portfóliók: kis cégek, sok beruházás, alacsony profitabilitás.
- A HML redundancia mintaspecifikus lehet (US 1963–2013).

## Kapcsolódás a factor trading rendszerhez

Az FF5 az alapvető keretrendszer, amelyhez képest factor exposure-t mérünk. Bármilyen portfólió vagy stratégia teljesítményét az FF5 faktorokra regresszálva tudjuk szétbontani alpha-ra és faktor hozamokra.
