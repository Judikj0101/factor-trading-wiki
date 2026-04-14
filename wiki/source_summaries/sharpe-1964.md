---
type: source_summary
tags: [capm, factor-model, cross-section]
confidence: high
last_reviewed: 2026-04-14
related: [[entities/capm]], [[entities/beta]], [[entities/market-risk-premium]], [[entities/alpha]]
---

# Sharpe (1964) — Capital Asset Prices: A Theory of Market Equilibrium Under Conditions of Risk

**Szerző:** William F. Sharpe
**Megjelenés:** 1964, The Journal of Finance, Vol. XIX, No. 3, 425–442
**DOI:** 10.1111/j.1540-6261.1964.tb02865.x
**Raw forrás:** `raw/papers/CAPITAL ASSET PRICES_ A THEORY OF MARKET EQUILIBRIUM UNDER CONDITIONS OF RISK_.md`

## Fő állítások

1. A **Capital Market Line (CML)** definiálja a kockázat és hozam közötti egyensúlyi kapcsolatot: magasabb hozam csak magasabb kockázat vállalásával érhető el.
2. A piac két árat kínál: az **idő árát** (kockázatmentes ráta) és a **kockázat árát** (extra hozam egységnyi kockázatra).
3. Diverzifikáció révén az idioszinkratikus kockázat eltüntethető → csak a **szisztematikus kockázat** (béta) releváns az árazásban.
4. Az elvárt hozam lineárisan függ a bétától:

$$E(R_i) = R_F + \beta_i \cdot [E(R_M) - R_F]$$

## Elméleti kontextus

- Markowitz (1952) portfólió-szelekciós modelljére épít: mean-variance optimalizálás
- Tobin (1958) separation theorem-jét kiterjeszti: a super-efficient portfólió = a piaci portfólió
- A CAPM az első formális **egyensúlyi asset pricing modell**

## Feltevések

- Befektetők mean-variance optimalizálók
- Homogén várakozások
- Korlátlan kölcsönzés/hitelezés $R_F$-en
- Nincs tranzakciós költség, adó, piaci súrlódás

## Hatás

- A CAPM lett a modern pénzügyi elmélet alapja
- A béta fogalma innen ered → [[entities/beta]]
- Később empirikusan megcáfolva (size effect, value effect) → [[entities/fama-french-five-factor-model]]
- Sharpe 1990-ben Nobel-díjat kapott (Markowitz-cal és Miller-rel együtt)

## Limitációk

- A feltevések irreálisak (homogén várakozások, korlátlan tőkeáttétel)
- Empirikusan: a béta **nem** magyarázza jól a cross-section hozamokat (Fama & French 1992)
- Ennek ellenére a CAPM továbbra is alapvető keretrendszer (WACC, oktatás)

## Források

- [[source_summaries/fama-french-1993]] — az FF3 motivációja a CAPM kudarcából ered
