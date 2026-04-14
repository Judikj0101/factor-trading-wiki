---
type: source_summary
tags: [statistics, backtesting, overfitting, cross-validation]
confidence: high
last_reviewed: 2026-04-14
related: [[entities/sharpe-ratio]], [[concepts/multiple-testing]], [[concepts/factor-zoo]], [[methodology/factor-validation]], [[source_summaries/bailey-lopez-de-prado-2014-dsr]], [[methodology/backtest-overfitting-detection]]
---

# Bailey, Borwein, Lopez de Prado & Zhu (2015) — The Probability of Backtest Overfitting

**Szerzok:** David H. Bailey, Jonathan M. Borwein, Marcos Lopez de Prado, Qiji Jim Zhu
**Megjelenes:** 2015, Journal of Computational Finance
**Raw forras:** `raw/papers/backtest-prob.md`

## Fo allitasok

1. **Probability of Backtest Overfitting (PBO):** altalanos keretrendszer annak meresere, hogy egy backteszt eredmenye mennyire megbizhato. A PBO annak a valoszinusege, hogy az in-sample (IS) optimalis strategia az out-of-sample (OOS) median ala teljesit.
2. **Combinatorially Symmetric Cross-Validation (CSCV):** egy konkret, nem-parametrikus, modell-fuggetlen implementacio a PBO becslesere.
3. **A holdout modszer 5 sulyos problemaja:**
   - A kutato valoszinuleg ismeri a holdout adatokat (tudatos vagy tudat alatti bias)
   - Kis mintanal sem az IS, sem az OOS nem megbizhato (< 1000 megfigyeles → < 20 ev heti adatokon)
   - Az OOS felhasznalasa csorbítja az IS-t (elveszitjuk a legfrissebb adatokat)
   - Magas varianciaju becslesi hiba (mas holdout mas kovetkeztetest ad)
   - Nem veszi figyelembe a probalkozasok szamat
4. **Overfitting definicio:** egy strategia-kivalasztasi folyamat overfit ha az IS-optimalis strategia varhato OOS rangja a median ala esik.

## A CSCV modszer

### Lepesek

1. **Adat felosztas:** a teljes idosort $S$ egyenlo reszre osztjuk ($S$ paros)
2. **Kombinaciok generalasa:** $\binom{S}{S/2}$ modon kombinaljuk a reszeket IS es OOS halmazba
3. **Strategia-kivalasztas IS-en:** minden IS-kombinacioban megkeressuk az optimalis strategiat (pl. max Sharpe ratio)
4. **OOS ertekeles:** az IS-optimalis strategia hogyan teljesit az OOS-en
5. **PBO szamitas:** hany kombinacioban teljesit az IS-optimalis strategia az OOS median ala

### Formalis definicio

$$PBO = \sum_{n=1}^{N} Prob[r_n^* < N/2 \mid r \in \Omega_n^*] \cdot Prob[r \in \Omega_n^*]$$

Ahol:
- $r_n^*$: a strategia $n$ OOS rangja
- $\Omega_n^* = \{f \in \Omega \mid f_n = N\}$: azon permutaciok halmaza ahol a strategia $n$ IS-optimalis
- $N$: strategiak szama

## Miert jobb mint a holdout?

| Szempont | Holdout | CSCV |
|---|---|---|
| Fix OOS | Igen (1 fele osztas) | Nem (minden kombimacio) |
| Fuggetlen a kutato ismereteitol | Nem | Igen (szisztematikus csere) |
| Figyelembe veszi N-t | Nem | Igen (implicit) |
| Parametrikus felteveseek | Nincs | Nincs (nem-parametrikus) |
| Output | Szignifikans / nem | Valoszinuseg (0-1) |

## Kapcsolodas a DSR-hez

A PBO es a [[source_summaries/bailey-lopez-de-prado-2014-dsr|DSR]] komplementerek:
- **DSR:** parametrikus teszt, kevesebb adatot igenyel, a Sharpe ratio-ra specifikus
- **PBO/CSCV:** nem-parametrikus, barmilyen teljesitmenymeroszohoz alkalmazhato, de sok adatot igenyel

## Limitaciok

- Nagy mintameret szukseges (sok reszre osztas + sok strategia)
- Szamitasigenyes: $\binom{S}{S/2}$ kombimacio exponencialisan no
- Nem kulon a strategia specifikus overfitting es a piaci rezsimlaltas hatasa
- Feltetelezi hogy az idosor stacionarius a reszperiodusok kozott

## Kapcsolodas a rendszerhez

A PBO keretrendszer a [[methodology/backtest-overfitting-detection]] egyik legfontosabb eszkuze. A [[methodology/factor-validation]] 3. lepesenel (out-of-sample validacio) a CSCV robusztusabb alternativat kinal a holdout-nal. A [[concepts/multiple-testing]] problemajat kozvetlenul kezeli, mert az IS/OOS csere automatikusan "latja" a probalkozasok szamat.
