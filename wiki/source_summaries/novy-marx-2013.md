---
type: source_summary
tags: [factor-model, profitability, value, cross-section, rmw]
confidence: high
last_reviewed: 2026-04-15
related: [[entities/rmw]], [[entities/hml]], [[entities/fama-french-five-factor-model]], [[concepts/value-premium]], [[source_summaries/fama-french-2014]]
---

# Novy-Marx (2013) — The Other Side of Value: The Gross Profitability Premium

**Forrás:** Journal of Financial Economics, 108(1), 1–28, 2013  
**Szerző:** Robert Novy-Marx (Simon Graduate School of Business, University of Rochester)  
**Fájl:** `raw/raw/Novy-Marx_Gross-Profitability-Anomaly_JFE_2013.pdf`

## Fő állítás

A **bruttó nyereségesség** (gross profits-to-assets = GP/A) a könyv/piaci arányhoz (B/M) hasonló erővel jósolja meg a részvényhozamokat a keresztmetszetben. A két tényező **komplementer**: együtt alkalmazva erősebb stratégiát adnak, mint külön-külön.

## Mértékegység

$$GP/A = \frac{\text{Revenues} - \text{Cost of Goods Sold}}{\text{Total Assets}}$$

Szemben a nettó nyereséggel (net income), a bruttó nyereségesség kevésbé torzított könyvelési manipulációkkal és a befektetési döntésekkel.

## Főbb eredmények

1. **Predikciós erő:** A GP/A és a B/M a keresztmetszeti hozamokat közel azonos mértékben magyarázza — mindkettő szignifikáns Fama-MacBeth regresszióban, egymás kontrollja mellett is.
2. **Komplementaritás:** A nyereséges cégek általában **growth részvények** (alacsony B/M) — ezért a profitability stratégia **kiváló hedge** a value stratégiának. Együttes alkalmazásuk csökkenti a volatilitást anélkül, hogy az átlaghozam csökkenne.
3. **Growth részvény paradoxon:** A profitabilis cégek átlagosan magasabb értékeltséggel bírnak (alacsonyabb B/M), mégis magasabb hozamot termelnek — ez nehezen egyeztethető a hagyományos value premium magyarázatokkal.
4. **Anomáliák magyarázata:** Egy négy-faktoros modell (piac + ipar-adjustált value + momentum + gross profitability) kimagaslóan teljesít különféle ismert anomáliák magyarázatában (ROE, default risk, net stock issuance, organizational capital).
5. **Méret-kontrol:** A gross profitability hatása fennmarad a legnagyobb, leglikvidabb részvényeknél is — nem mikroméretű részvény-effektus.

## Elméleti keret

- A dividend discount modellből levezethető: ha $B/M$ magasabb várható hozamot jelez, akkor a magasabb jövőbeli jövedelmezőség is magasabb várható hozammal kell, hogy járjon (ceteris paribus).
- Konzisztens mind a kockázatalapú, mind a behavioral (félreárazás) magyarázatokkal.

## Kapcsolata az FF5-tel

Ez a paper **közvetlen előfutára** a Fama-French (2014) RMW faktorának:
- Fama & French (2014) az RMW-t (Robust Minus Weak profitability) részben Novy-Marx eredményeire alapozzák
- A különbség: FF5 operating profitability-t használ (GP − SGA − D&A), Novy-Marx gross profitability-t (GP = Revenue − COGS)
- Gross profitability empirikusan **erősebb** jel, de kevésbé elméletileg motivált

## KKE relevanciája

- Az earnings quality (NI/CFO) faktor, amelyet Foye et al. (2016) az SMB helyettesítőjeként javasol KKE-ban, részben a profitability dimenzióhoz kapcsolódik
- A gross profitability hatása teszteletlen KKE piacokon — nyitott kérdés: [[open_questions/kke-factor-premiums]]

## Kapcsolódó wiki oldalak

- [[entities/rmw]] — az FF5 profitability faktora
- [[entities/hml]] — komplementer value faktor
- [[source_summaries/fama-french-2014]] — Novy-Marx eredményeire épít
- [[concepts/value-premium]] — a profitability a value prémium "másik oldala"
