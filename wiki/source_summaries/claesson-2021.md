---
type: source_summary
tags: [factor-model, emerging-markets, cross-section, regression]
confidence: medium
last_reviewed: 2026-04-14
related: [[entities/fama-french-five-factor-model]], [[entities/smb]], [[entities/hml]], [[entities/rmw]], [[entities/cma]], [[entities/momentum]], [[concepts/factor-zoo]], [[open_questions/kke-factor-premiums]]
---

# Claesson (2021) — The Fama-French Asset Pricing Models: Emerging Markets

## Bibliográfia

- **Szerzo:** Henrik Claesson
- **Tipus:** Master's Thesis, Uppsala University
- **Ev:** 2021
- **Forras fajl:** `raw/papers/FULLTEXT01.md`

## Fo allitasok

1. A Fama-French harom-, ot- es hatfaktoros modelleket teszteli **26 fejlodo orszag** tozsdejen, 1992. julius es 2021. julius kozott (Kenneth R. French Data Library adataival).
2. A **size (SMB) es investment (CMA) faktorok redundansak** fejlodo piacokon — nem adnak szignifikans hozzaadott magyarazo erot.
3. A **value (HML) es profitability (RMW)** faktorok a legfontosabb hozamhajtok fejlodo piacokon.
4. A haromfaktoros modell **valamivel szignifikansabb** eredmenyeket produkalt, de az otfaktoros modell **jobb magyarazo ero** (R-squared) szempontjabol.
5. A hatfaktoros modell (momentum hozzaadasaval) a momentum-szortolt portfolioknal dominal, de **osszessegeben insignifikans**.
6. Az otfaktoros modell **eletkepes alternativa** a haromfaktoroshoz kepest fejlodo piacokon.

## Relevans eredmenyek a factor trading rendszerhez

- **KKE vonatkozas:** a 26 fejlodo orszag kozott valoszinuleg szerepelnek KKE orszagok is (a French Data Library emerging markets kategoriaja tartalmaz KKE regiokat), de az aggregalt emerging market eredmenyek elfedhetik a regionalis kulonbsegeket.
- **SMB gyengesege** osszhangban van a Foye et al. (2016) eredmenyeivel az EE EU orszagokra.
- A **value premium** megjelenik fejlodo piacokon — ez fontos jelzes a [[concepts/value-premium]] fenntarthatosagahoz.

## Limitaciok

- Aggregalt emerging market adatokat hasznal — nincs KKE-specifikus bontás.
- A Kenneth French Data Library adatai lehetnek torzitotak (survivorship bias, adatminoseg fejlodo piacokra).
- GRS teszt formálisan elutasitja mindharom modellt.
- A hatfaktoros modell eredmenyei insignifikansak — nem kínál javulást az otfaktoroshoz kepest.
