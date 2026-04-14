---
type: methodology
tags: [backtesting, overfitting, cross-validation, statistics]
confidence: high
last_reviewed: 2026-04-14
related: [[methodology/deflated-sharpe-ratio]], [[methodology/factor-validation]], [[methodology/cross-validation]], [[methodology/backtesting]], [[concepts/multiple-testing]], [[source_summaries/bailey-borwein-lopez-de-prado-zhu-2015-pbo]], [[source_summaries/bailey-lopez-de-prado-2014-dsr]]
---

# Backtest Overfitting Detection — Backteszt overfitting felismeres

## Mikor hasznaljuk

Barmilyen szisztematikus strategia backteszt eredmenyeinek ertekelese soran, kulonosen ha:
- Tobb strategia-konfiguriaciot teszteltunk
- Az IS performance "tul jo" (gyanus Sharpe ratio, monoton equity curve)
- Nincs independent OOS validacio

## Mi az overfitting a backteszt kontextusban?

**Definicio (Bailey et al. 2015):** Egy strategia-kivalasztasi folyamat overfit ha az in-sample optimalis strategia varhato out-of-sample rangja a median ala esik.

Informallisan: a strategia a zajt tanulta meg, nem a jelet. Penzugyi idosorokban ez kuluonosen veszelyes a **memory effects** miatt — az overfit strategia nem csak alulteljesit, hanem aktivan veszit (a memoria "visszaforditja" a random mintazatokat amikre az overfit strategia epitett).

## Eszkoztar

### 1. Deflated Sharpe Ratio (DSR)

Ld. reszletesen: [[methodology/deflated-sharpe-ratio]]

**Mikor:** kevesebb adat, egyetlen kivalasztott strategia ertekelese
**Elony:** parametrikus, gyors, kevesebb adat kell
**Hatrany:** Sharpe ratio-specifikus, feltetelezi a probak SR-normaalitasat

### 2. Probability of Backtest Overfitting (PBO / CSCV)

Ld. reszletesen: [[source_summaries/bailey-borwein-lopez-de-prado-zhu-2015-pbo]]

**Lepesek:**
1. Osszes strategia-konfiguracio backtesztelese
2. Az idosor feloszlasa S egyenlo reszre
3. $\binom{S}{S/2}$ kombinacio generalasa IS/OOS felosztasokhoz
4. Minden felosztasban: IS-optimalis strategia OOS rangjanak merese
5. PBO = hanyadreszben teljesit az IS-optimalis a median alatt OOS-ben

**Mikor:** sok adat, tobb strategia osszehasonlitasa
**Elony:** nem-parametrikus, barmilyen performance meroszohoz
**Hatrany:** szamitasigenyes, sok adat kell

### 3. Performance degradation vizsgalat

Az IS es OOS performance kulombsegenek rendszeres vizsgalata:
- Ha az IS-bol az OOS-be valo atlagesben a performance szisztematikusan csokken → overfitting gyanuja
- Vizualizacio: IS rank vs OOS rank scatter plot

### 4. Minimum Backtest Length (MinBTL)

Mennyi adatra van szuekszeg ahhoz, hogy egy adott Sharpe ratio szignifikaans legyen?

$$MinBTL \approx 1 + \left[1 - \hat{\gamma}_3 \cdot SR + \frac{\hat{\gamma}_4 - 1}{4} \cdot SR^2\right] \cdot \left(\frac{Z_\alpha}{SR - SR_0}\right)^2$$

Ha a meglevó minta roviudebb mint MinBTL → az eredmeny nem megbizhato.

## Donxtesi fa

```
Backteszt eredmeny ertekelese
├── Hany konfiguriaciot teszteltunk? (N)
│   ├── N = 1 → Standard PSR / t-teszt
│   └── N > 1 → DSR vagy PBO alkalmazasa
├── DSR > 0.95?
│   ├── Igen → Tovabb az OOS validaciora
│   └── Nem → Elvetni vagy N csokkentese (kevesebb proba)
├── PBO < 0.50?
│   ├── Igen → Megbizhato (de OOS meg mindig kell!)
│   └── Nem → Overfit → uj megkozellites
└── MinBTL < T?
    ├── Igen → Minta elegendo
    └── Nem → Tobb adat kell
```

## Holdout modszer buktatoi

A holdout (train/test split) **nem megfelelo vedelem** az overfitting ellen:
1. A kutato ismerheti az OOS adatokat (tudatos vagy tudat alatti)
2. Kis mintanal mindket felkeez tul rovid
3. Az OOS "felemeszti" az IS-t
4. Magas varianciaju becsles (mas split → mas eredmeny)
5. Nem veszi figyelembe N-t (a probalkozasok szamat)

**Megoldas:** CSCV (minden IS/OOS kombimacio szisztematikus vizsgalata) vagy DSR (parametrikus korrekcion).

## Gyakori hibak

- **"Szep equity curve" = jo strategia:** az overfit strategiak is szep IS equity curve-ot adnak
- **Egyetlen OOS teszt mint bizonyitek:** egyetlen holdout nem elegendo
- **Informalis probak figyelmen kivul hagyasa:** ha "csak" 10 formalis tesztet futtattunk, de informaliisan 100-at → N = 100
- **Tranzakcious kooltsegek elhanyagolasa:** az overfitting hajlamos magas turnover-u strategiakat talalni

## Forrasok

- [[source_summaries/bailey-borwein-lopez-de-prado-zhu-2015-pbo]]
- [[source_summaries/bailey-lopez-de-prado-2014-dsr]]
- [[source_summaries/simonian-2024-model-validation]]
