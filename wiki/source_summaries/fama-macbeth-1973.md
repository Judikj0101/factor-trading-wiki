---
type: source_summary
tags: [methodology, cross-section, capm, statistics, regression]
confidence: high
last_reviewed: 2026-04-15
related: [[methodology/fama-macbeth-regresszio]], [[entities/capm]], [[entities/beta]], [[source_summaries/shanken-zhou-2006]], [[source_summaries/fama-french-1992]]
---

# Fama & MacBeth (1973) — Risk, Return, and Equilibrium: Empirical Tests

**Forrás:** Journal of Political Economy, 81(3), 607–636, 1973  
**Szerzők:** Eugene F. Fama, James D. MacBeth  
**Fájl:** `raw/raw/Fama-Macbeth.pdf` (scanned)

## Fő állítás

A tőkepiaci egyensúly (CAPM) empirikus tesztelésére kétlépéses keresztmetszeti regressziós eljárást fejlesztenek ki, amelyet **Fama-MacBeth (FM) regresszió** névvel ismer az irodalom. Ezzel igazolják, hogy 1926–1968 között a béta és a várható hozam között pozitív, lineáris kapcsolat áll fenn.

## A Fama-MacBeth kétlépéses eljárás

### 1. lépés — Idősoros bétabecslés (time-series)
- Minden részvény (vagy portfólió) hozamát regresszálják a piaci hozamra
- Becslik az egyedi bétát: $\hat{\beta}_i = \frac{Cov(R_i, R_M)}{Var(R_M)}$
- Ajánlott: portfóliók alkalmazása az EIV (errors-in-variables) probléma csökkentésére

### 2. lépés — Keresztmetszeti regresszió (cross-section)
Minden $t$ időpontban:
$$R_{i,t} = \gamma_{0,t} + \gamma_{1,t}\hat{\beta}_i + \gamma_{2,t}\hat{\beta}_i^2 + \gamma_{3,t}\sigma^2(\epsilon_i) + \epsilon_{i,t}$$

- $\gamma_{1,t}$: a kockázati prémium becslése az adott hónapban
- $\gamma_{2,t}$: nemlinearitás tesztje (ha szignifikáns: a béta-hozam kapcsolat nem lineáris)
- $\gamma_{3,t}$: idiosynkratikus kockázat hatása (CAPM szerint 0 kell legyen)

### Inferencia
- A $\gamma$ koefficiensek **idősorát** átlagolják
- Standard error: az átlagos koefficiens időbeli szórásából:
$$SE(\bar{\gamma}) = \frac{SD(\gamma_t)}{\sqrt{T}}$$
- Ez automatikusan kezeli a keresztmetszeti korreláció problémáját (Newey-West nem szükséges)

## Főbb eredmények (1926–1968)

1. **Béta és hozam:** Pozitív, szignifikáns kapcsolat — a béta prémium statisztikailag szignifikáns
2. **Linearitás:** A $\gamma_2$ (béta négyzete) nem szignifikáns → a kapcsolat lineáris
3. **Idiosynkratikus kockázat:** Nem szignifikáns → a diverzifikálható kockázat nem árazódik be
4. **Összesség:** Az adatok konzisztensek a CAPM-mel az 1926–1968 időszakban

## Relevanciája a wiki számára

- Az **FM regresszió a cross-sectional faktor vizsgálatok standard eszköze** — minden Fama-French paper ezt alkalmazza
- A [[source_summaries/fama-french-1992]] is FM regressziót használ — és megcáfolja, hogy a béta magyarázza a hozamot
- A [[methodology/fama-macbeth-regresszio]] részletesen leírja az eljárást
- Limitáció: az EIV-probléma torzítja a béta becslést → megoldás portfóliók alkalmazása (Shanken 1992 korrekció)
- Megjegyzés: scanned PDF, szöveges tartalom nem kinyerhető — source summary saját tudás alapján

## Kapcsolódó wiki oldalak

- [[methodology/fama-macbeth-regresszio]] — az eljárás részletes leírása
- [[entities/capm]] — amelyet ez a paper tesztel
- [[entities/beta]] — az első lépés outputja
- [[source_summaries/shanken-zhou-2006]] — az FM eljárás szimulációs értékelése
- [[source_summaries/fama-french-1992]] — FM alkalmazása, béta megcáfolása
