---
type: entity
tags: [factor-model, cross-section, momentum]
confidence: high
last_reviewed: 2026-04-14
related: [[entities/fama-french-five-factor-model]], [[entities/capm]], [[entities/momentum]], [[entities/smb]], [[entities/hml]], [[entities/alpha]], [[source_summaries/kruger-2007]]
---

# Carhart Four-Factor Model

## Definíció

Carhart (1997) bővítése a Fama-French háromfaktoros modellnek egy momentum faktorral (WML/MOM). A mutual fund teljesítmény értékelés de facto standardja.

$$R_{it} - R_{Ft} = \alpha_i + b_i(R_{Mt} - R_{Ft}) + s_i \cdot SMB_t + h_i \cdot HML_t + m_i \cdot MOM_t + e_{it}$$

## Faktorok

| Faktor | Leírás |
|---|---|
| $R_M - R_F$ | [[entities/market-risk-premium\|Piaci kockázati prémium]] |
| [[entities/smb\|SMB]] | Size faktor |
| [[entities/hml\|HML]] | Value faktor |
| MOM (WML) | [[entities/momentum\|Momentum faktor]]: winners − losers (12-2 havi hozam) |

## Miért fontos

- A Carhart modell az első széles körben elfogadott keretrendszer a **momentum** faktor formális beépítésére
- Mutual fund alpha mérés: ha egy alap "alpha"-ja a Carhart modellel mérve nulla, az alap nem termel valódi hozzáadott értéket — csak faktor exposure-ért "fizet" (Kruger 2007 megerősíti)
- Az FF5 **nem tartalmazza** a momentumot → a Carhart modell kiegészítő marad

## Carhart vs FF5

| Aspektus | Carhart 4F | FF5 |
|---|---|---|
| Faktorok | Market + SMB + HML + MOM | Market + SMB + HML + RMW + CMA |
| Momentum | Igen | Nem |
| Profitability | Nem | Igen (RMW) |
| Investment | Nem | Igen (CMA) |
| Használat | Fund evaluation | Asset pricing tesztelés |

A két modell kiegészíti egymást. FF5 + MOM ("FF6") is létezik informálisan.

## Források

- [[source_summaries/carhart-1997]]
- [[source_summaries/kruger-2007]]
- [[source_summaries/msci-foundations-2013]]
