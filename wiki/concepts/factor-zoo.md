---
type: concept
tags: [factor-model, overfitting, statistics, cross-section]
confidence: high
last_reviewed: 2026-04-14
related: [[concepts/multiple-testing]], [[source_summaries/harvey-liu-zhu-2016]], [[entities/fama-french-five-factor-model]], [[methodology/factor-validation]]
---

# Factor Zoo

## Mi ez

A "factor zoo" a pénzügyi irodalomban dokumentált faktorok elszaporodására utal. Harvey, Liu & Zhu (2016) 316 különböző faktort katalogizált 313 publikált cikkből. A probléma: ha több száz faktort tesztelünk, a véletlen folytán is sok "szignifikánsnak" tűnik.

## Miért fontos

- A factor zoo a **data mining / p-hacking** probléma megnyilvánulása az asset pricing-ben.
- A szokásos t > 2.0 küszöb hamis felfedezéshez vezet ha sok teszt fut.
- Harvey et al. (2016) szerint a helyes küszöb **t > 3.0** új faktorokra.
- "Most claimed research findings in financial economics are likely false."

## A probléma gyökere

1. **Publication bias:** nem-szignifikáns eredmények nem jelennek meg.
2. **Hidden tests:** a kutatók sok változatot próbálnak, de csak a "működőt" publikálják.
3. **Data snooping:** ugyanazt az adathalmazt használják újra és újra.
4. **Replication crisis:** pénzügyi replikációs tanulmányok ritkák (szemben az orvostudománnyal).

## Megoldási irányok

- **Multiple testing correction:** Bonferroni, Holm, BH (False Discovery Rate)
- **Out-of-sample validáció:** más periódus, más piacok
- **Elméleti motiváció:** elméletből levezetett faktoroknak alacsonyabb küszöb, de t > 2.0 soha nem elég
- **Replikáció más asset class-okban:** Asness et al. (2013), Koijen et al. (2012)

## Érintett entitások

- [[entities/fama-french-five-factor-model]] — az FF5 faktorok elméleti motivációjúak (DDM) → erősebb, de nem mentesek a kritikától
- [[entities/smb]] — a size prémium különösen vitatott a zoo kontextusban

## Kapcsolodo eszkozok

- [[methodology/deflated-sharpe-ratio]]: a Sharpe ratio korrekcioja a factor zoo kontextusaban
- [[methodology/backtest-overfitting-detection]]: PBO/CSCV az overfitting valoszinusegenek meresere

## Források

- [[source_summaries/harvey-liu-zhu-2016]]
- [[source_summaries/bailey-lopez-de-prado-2014-dsr]]
