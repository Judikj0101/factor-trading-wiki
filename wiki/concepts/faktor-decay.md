---
type: concept
tags: [factor-zoo, multiple-testing, backtesting, statistics, factor-model]
confidence: high
last_reviewed: 2026-04-15
related: [[concepts/factor-zoo]], [[concepts/multiple-testing]], [[methodology/factor-validation]], [[methodology/backtest-overfitting-detection]], [[source_summaries/mclean-pontiff-2015]], [[source_summaries/harvey-liu-zhu-2016]]
---

# Faktor Decay (Faktorerodáció)

## Mi ez

A **faktor decay** az a jelenség, amikor egy dokumentált faktorra épülő stratégia hozama az idő előrehaladtával — különösen publikáció után — szisztematikusan csökken. Ez az egyik legnagyobb gyakorlati kockázata a faktoralapú befektetésnek.

## A McLean & Pontiff (2015) bizonyíték

97 cross-sectional prediktor vizsgálatán alapuló empirikus evidencia:

| Periódus | Hozamcsökkentés |
|---|---|
| Out-of-sample | −26% |
| Post-publikáció | −58% |
| Tisztán publikáció-hatás | ~−32% |

A 26%-os OOS csökkenés felső korlátja az in-sample statisztikai torzításnak (data mining, szelekciósfeltételek). A maradék 32% a befektetők tanulásának tudható be.

## Mechanizmusok

### 1. Statisztikai torzítás (data snooping)
- Az in-sample t-statisztika felfelé torzított, ha sok faktort teszteltek és csak a szignifikánsakat közölték
- Kapcsolat: [[concepts/multiple-testing]], Harvey et al. (2016) t > 3.0 küszöb
- Ez magyarázza az OOS csökkenés egy részét

### 2. Befektetői tanulás (publication effect)
- A cikk megjelenése után szofisztikált befektetők (hedge fundok, quant deskok) elkezdik alkalmazni a stratégiát
- Az arbitrázs csökkenti a félreárazást → a prémium összezsugorodik
- **Bizonyíték:** Short interest és kereskedési volumen növekszik publikáció után (McLean & Pontiff)

### 3. Kockázat-alapú csökkenés
- Ha a prémium kockázatalapú volt, és a mögöttes kockázat csökkent (pl. piaci integráció mélyülése), a prémium is csökken
- Ez nem "decay" a szó szoros értelmében — a prémium jogosan csökkent

## Decay sebessége

- A decay **nem azonnali** — évekig is eltarthat
- Lassabb, ha: a részvények illikvidek, magas az idiosynkratikus kockázat, nehezen replikálható a stratégia
- Gyorsabb, ha: likvid részvények, egyszerű megvalósítás, magas in-sample t-statisztika

## Következmények a faktor validációra

1. **Konzervatívabb küszöb:** Harvey et al. (2016) t > 3.0 nem elegendő — még ez felett is 58%-os post-pub csökkenés várható
2. **OOS teszt kötelező:** Minden faktort valódi out-of-sample adaton kell tesztelni
3. **Live trading eredmények fontosabbak, mint backtest** — a backtest óhatatlanul tartalmaz data mining torzítást
4. **Portfólió szintű decay tracking:** Élő stratégián rendszeresen ellenőrizni, hogy az IR csökken-e

## KKE relevanciája

A KKE piacok ebből a szempontból **kedvezőbb** pozícióban vannak:
- Kisebb piac → kevesebb tőke arbitrálhat → lassabb decay
- Kevesebb publikált KKE-specifikus faktor → kisebb verseny
- Alacsonyabb likviditás → magasabb tranzakciós költség → arbitrázs korlátozott
- **Caveat:** A kisebb minta méret miatt a data mining torzítás is nagyobb lehet

## Kapcsolódó wiki oldalak

- [[concepts/factor-zoo]] — a 316+ faktor összefüggése
- [[concepts/multiple-testing]] — statisztikai torzítás forrása
- [[methodology/factor-validation]] — a validáció eljárása
- [[methodology/backtest-overfitting-detection]] — PBO/DSR eszközkészlet
- [[source_summaries/mclean-pontiff-2015]] — fő empirikus forrás
- [[source_summaries/harvey-liu-zhu-2016]] — komplementer statisztikai kritika
