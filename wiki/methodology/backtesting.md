---
type: methodology
tags: [backtesting, performance, risk-management]
confidence: high
last_reviewed: 2026-04-14
related: [[methodology/factor-validation]], [[methodology/cross-validation]], [[methodology/backtest-overfitting-detection]], [[methodology/deflated-sharpe-ratio]], [[entities/sharpe-ratio]], [[source_summaries/simonian-2024-model-validation]]
---

# Backtesting — Backteszt vegrehajtasa

## Mikor hasznaljuk

Barmilyen befektetesi strategia vagy modell historikus tesztelesenel. A backteszt a validacios pipeline elso lepese — szukseges de **nem elegseges** eszkoz.

## Elofeltetelek

- Egyertelmuen definialt strategia (signal, entry/exit, poziciomeretezes)
- Megfelelo minosegu es hosszusagu historikus adat
- Tisztaban lenni a lehetseges torzitasokkal (survivorship, look-ahead, selection bias)

## Az idealis backteszt felepitese (Simonian 2024)

### 1. Adatkivalasztas

- **Idoszak hossza:** nincs univerzalisan helyes ertek — a gazdasagi relevanciat kell merlegelni
  - Tul hosszu → elavult piaci korulmenyek (pl. 1930-as evek)
  - Tul rovid → nem megbizhato statisztika
- **Adat minoseg:** ellenorizni hianyzo, duplikalt, hibas ertekek → kulombozo vendor osszevetes
- **Regime-switching modellek** segithetnek az idosor okomai felosztasaban (Hamilton 1989, Filardo 1994)

### 2. Backteszt komponensek

| Komponens | Leiras | Tipikus hiba |
|---|---|---|
| **Signal(ok)** | A modell altal generalt jelzes | Kulon es egyutt is tesztelni |
| **Entry/exit szabalyok** | Mikor nyitunk/zarunk poziciot | Tul sok parameter → overfitting |
| **Poziciomeretezes** | Mennyit kereskedunk | Koncentralt tradek → hamis eredmeny |
| **Rebalancing** | Portfolio suly visszaallitas | Frekvencia hatas vizsgalata |

### 3. Futatas: In-sample vs Out-of-sample

- **In-sample (IS):** a modell fejlesztesere hasznalt idoszak — **soha nem tekintheto validacionak**
- **Out-of-sample (OOS):** kulon, kronologiailag kesobbi idoszak — ez az igazi teszt
- Ld. reszletesen: [[methodology/cross-validation]]

### 4. Eredmenyek ertekelese

Metrics amikra figyelni kell:
- [[entities/sharpe-ratio]] (de figyelemmel a DSR-re: [[methodology/deflated-sharpe-ratio]])
- Sortino ratio (downside risk)
- Maximum drawdown es recovery time
- Skewness es kurtosis
- Trade count es win rate → ne fugjjon nehany "lucky trade"-tol
- Tranzakcious koltsegek hatasa (spread, market impact, commission)

## Buktatók (pitfalls)

### Statisztikai buktatók
- **Overfitting:** alacsony bias, magas variancia — a modell a zajt tanulja meg → [[methodology/backtest-overfitting-detection]]
- **Data snooping:** sok modellvaltozat → a legjobb megtalallasa garantalt
- **Multiple testing:** a [[concepts/multiple-testing]] korrekciok nelkul a p-ertekek ertektelenek

### Adat-buktatok
- **Survivorship bias:** csak tulelok bevonasa → felfelele torzitas
- **Look-ahead bias:** jovobeli informacio hasznalata (akár tudattalanul — pl. GFC utani "risk radar")
- **Inception point risk:** mas kiindulopont → mas eredmeny (selection bias tipusa)

### Megvalositasi buktatok
- **Tranzakcious koltsegek:** spread + market impact + commission erodalhattja a hozamot
- **Execution lag:** t idopontu signal → t+1 vagy t+2 kereskedes (realisztikus felteteleves!)
- **Koncentracio:** ha a hozam nehany trade-bol jon → nem generalizalhato
- **Kapacitas:** a strategia mukodik kis mereten, de skalalodik-e?

## Kapcsolodas a validacios pipeline-hoz

```
1. Backteszt (ez az oldal)
   ↓
2. Cross-validation → [[methodology/cross-validation]]
   ↓
3. Overfitting detection → [[methodology/backtest-overfitting-detection]]
   ↓
4. Factor validation (t > 3.0) → [[methodology/factor-validation]]
   ↓
5. Stress testing / scenario analysis
   ↓
6. Live paper trading / OOS monitoring
```

## Forrasok

- [[source_summaries/simonian-2024-model-validation]]
- [[source_summaries/bailey-lopez-de-prado-2014-dsr]]
- [[source_summaries/bailey-borwein-lopez-de-prado-zhu-2015-pbo]]
