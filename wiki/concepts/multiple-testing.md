---
type: concept
tags: [statistics, overfitting, factor-model]
confidence: high
last_reviewed: 2026-04-15
related: [[concepts/factor-zoo]], [[concepts/faktor-decay]], [[source_summaries/harvey-liu-zhu-2016]], [[source_summaries/mclean-pontiff-2015]], [[methodology/factor-validation]]
---

# Multiple Testing (Többszörös tesztelés)

## Mi ez

Statisztikai probléma: ha egyszerre sok hipotézist tesztelünk, a hamis pozitívok valószínűsége drasztikusan nő. A factor investing-ben ez azt jelenti, hogy ha 316 faktort tesztelsz t > 2.0 küszöbbel, sok "szignifikáns" eredmény valójában véletlen.

## Miért fontos

- A faktor kutatás lényegében egy hatalmas multiple testing exercice.
- A szokásos 5% szignifikancia szint (t ≈ 2.0) egy teszt esetén van kalibrálva.
- 316 tesztnél a Bonferroni korrekció: $\alpha_{adj} = 0.05 / 316 \approx 0.00016$ → t > 3.8
- Harvey et al. (2016) pragmatikus javaslata: **t > 3.0** mint minimum

## Két fő kontroll-módszer

### 1. Family-Wise Error Rate (FWER)
- Annak valószínűsége, hogy **legalább egy** hamis felfedezés történik
- Konzervatív (Bonferroni, Holm)
- Alkalmas ha egyetlen hamis felfedezés sem megengedhető

### 2. False Discovery Rate (FDR)
- A hamis felfedezések **várható aránya** az összes felfedezéshez képest
- Kevésbé szigorú (Benjamini-Hochberg)
- Alkalmas ha néhány hamis pozitív elfogadható, ha a többség valódi

## Gyakorlati alkalmazás

Új faktor/signal értékelésénél:
1. Mi a t-statistic? Ha < 3.0, erős kétely.
2. Hány más faktort teszteltek/teszteltünk korábban? (a küszöb növekszik)
3. Van-e elméleti motiváció? (ha igen, enyhébb küszöb de soha nem t < 2.0)
4. Van-e out-of-sample validáció? (más periódus, más piac)

## Kapcsolodo eszkozok

- [[methodology/deflated-sharpe-ratio]]: a Sharpe ratio korrekcioja multiple testing-re
- [[methodology/backtest-overfitting-detection]]: PBO/CSCV keretrendszer
- [[methodology/backtesting]]: backteszt vegrehajtasi utmutato a buktatokkal

## Források

- [[source_summaries/harvey-liu-zhu-2016]]
- [[source_summaries/bailey-lopez-de-prado-2014-dsr]]
- [[source_summaries/bailey-borwein-lopez-de-prado-zhu-2015-pbo]]
