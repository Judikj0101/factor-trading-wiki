---
type: source_summary
tags: [factor-model, cross-section, regression]
confidence: high
last_reviewed: 2026-04-14
related: [[entities/fama-french-five-factor-model]], [[entities/smb]], [[entities/hml]], [[entities/rmw]], [[entities/cma]], [[entities/market-risk-premium]], [[concepts/value-premium]], [[open_questions/hml-redundancy]]
---

# Fama & French (2014) — A Five-Factor Asset Pricing Model

**Szerzők:** Eugene F. Fama, Kenneth R. French
**Megjelenés:** 2014, Journal of Financial Economics
**DOI:** [10.1016/j.jfineco.2014.10.010](https://doi.org/10.1016/j.jfineco.2014.10.010)
**Raw forrás:** `raw/papers/A five-factor asset pricing model.md`

## Fő állítások

1. A háromfaktoros modellt (Market, SMB, HML) két új faktorral bővítik: **RMW** (profitability) és **CMA** (investment).
2. Az ötfaktoros modell jobban magyarázza a részvényhozamok cross-section variációját, mint a háromfaktoros modell (71–94% magyarázott variancia).
3. A GRS teszt formálisan elutasítja a modellt, de a gyakorlati teljesítmény erős.
4. **Meglepő eredmény:** Ha RMW és CMA benne van a modellben, a HML (value faktor) **redundánssá** válik — az átlagos HML hozamot a többi faktornak való kitettség magyarázza.
5. A modell leggyengébb pontja: kis cégek, amelyek sokat fektetnek be alacsony profitabilitás mellett ("small stocks that invest a lot despite low profitability").

## Elméleti alap

A dividend discount model (DDM) alapján:
- Magasabb B/M → magasabb elvárt hozam (fix cashflow mellett)
- Magasabb várható profit → magasabb elvárt hozam
- Magasabb várható beruházás → **alacsonyabb** elvárt hozam

Ez a logika motiválja a profitability és investment faktorok hozzáadását.

## Faktor definíciók

| Faktor | Név | Konstrukció |
|--------|-----|-------------|
| $R_M - R_F$ | Market risk premium | Piaci hozam mínusz kockázatmentes ráta |
| SMB | Small Minus Big | Kis cégek hozama mínusz nagy cégek hozama |
| HML | High Minus Low | Magas B/M hozama mínusz alacsony B/M hozama |
| RMW | Robust Minus Weak | Magas profitabilitás mínusz alacsony profitabilitás |
| CMA | Conservative Minus Aggressive | Konzervatív beruházók mínusz agresszív beruházók |

## Regressziós keretrendszer

$$R_{it} - R_{Ft} = a_i + b_i(R_{Mt} - R_{Ft}) + s_i \cdot SMB_t + h_i \cdot HML_t + r_i \cdot RMW_t + c_i \cdot CMA_t + e_{it}$$

## Limitációk

- A HML redundancia eredmény **mintaspecifikus** lehet (US, 1963–2013) — a szerzők maguk figyelmeztetnek erre.
- A modell nem tartalmaz momentum faktort (szemben Carhart 1997-tel).
- A forrás clipping (nem teljes szöveg) — a részletes teszteredmények és táblázatok nem elérhetők.

## Kapcsolódás a rendszerhez

Ez a modell a factor investing elméleti alapja. A faktorok (SMB, HML, RMW, CMA) közvetlenül használhatók:
- Portfólió hozamok dekompozíciójára
- Alpha mérésre (az $a_i$ intercept)
- Faktor exposure tervezésre
