---
type: entity
tags: [factor-model, capm, cross-section]
confidence: high
last_reviewed: 2026-04-14
related: [[entities/market-risk-premium]], [[entities/beta]], [[entities/fama-french-five-factor-model]], [[entities/alpha]]
---

# CAPM (Capital Asset Pricing Model)

## Definíció

A Sharpe (1964), Lintner (1965) és Mossin (1966) által kidolgozott egyetlen-faktoros asset pricing modell. A modern pénzügyi elmélet alapköve.

$$E(R_i) = R_F + \beta_i \cdot [E(R_M) - R_F]$$

Ahol:
- $E(R_i)$: az $i$. részvény elvárt hozama
- $R_F$: kockázatmentes ráta
- $\beta_i$: a részvény szisztematikus kockázata (piaci béta)
- $E(R_M) - R_F$: a piaci kockázati prémium

## Fő állítások

1. Csak a szisztematikus (piaci) kockázat számít — az idioszinkratikus kockázat diverzifikálható
2. Az elvárt hozam lineárisan függ a bétától
3. Egyensúlyban a super-efficient portfólió = a piaci portfólió (Tobin separation theorem)

## Feltevések

- Befektetők mean-variance optimalizálók
- Homogén várakozások (mindenki ugyanazt gondolja)
- Korlátlan kölcsönzés/hitelezés a kockázatmentes rátán
- Nincs tranzakciós költség, adó
- Tökéletesen likvid piacok

## Empirikus problémák

A CAPM-et az 1970-es évektől kezdve számos anomália megcáfolta:
- **Size effect** (Banz 1981): kis cégek felülteljesítenek → [[entities/smb]]
- **Value effect** (Fama & French 1992): magas B/M részvények felülteljesítenek → [[entities/hml]]
- **Momentum** (Jegadeesh & Titman 1993): nyertesek nyernek → [[entities/momentum]]
- **Low volatility anomaly**: alacsony béta részvények felülteljesítenek → [[entities/low-volatility]]

Ezek az anomáliák motiválták a multi-faktor modellek fejlesztését: FF3 → Carhart 4F → [[entities/fama-french-five-factor-model|FF5]].

## Helye a modell evolúcióban

```
CAPM (1964) → FF3 (1993) → Carhart 4F (1997) → FF5 (2014)
   1 faktor      3 faktor     4 faktor       5 faktor
```

## Források

- [[source_summaries/sharpe-1964]] — az eredeti CAPM paper
- [[source_summaries/markowitz-1952]] — a portfólió-szelekciós elméleti alap
- [[source_summaries/msci-foundations-2013]]
- [[source_summaries/barra-use4-2011]]
