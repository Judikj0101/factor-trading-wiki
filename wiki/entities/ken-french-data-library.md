---
type: entity
tags: [factor-model, datasets, cross-section]
confidence: high
last_reviewed: 2026-04-14
related: [[entities/fama-french-five-factor-model]], [[entities/smb]], [[entities/hml]], [[entities/rmw]], [[entities/cma]], [[entities/momentum]]
---

# Ken French Data Library

## Definíció

Kenneth R. French (Dartmouth Tuck School) által fenntartott publikus adatbázis, amely a Fama-French faktor hozamokat és portfólió adatokat tartalmazza. A factor investing kutatás **elsődleges publikus adatforrása**.

**URL:** https://mba.tuck.dartmouth.edu/pages/faculty/ken.french/data_library.html

## Elérhető faktor adatok

| Adatkészlet | Tartalom | Frekvencia |
|---|---|---|
| **FF 3 Factors** | $R_M - R_F$, SMB, HML | napi, heti, havi |
| **FF 5 Factors (2×3)** | Market, SMB, HML, RMW, CMA | napi, havi |
| **Momentum (MOM)** | Winners − Losers | napi, havi |
| **ST Reversal** | Short-term reversal faktor | napi, havi |
| **LT Reversal** | Long-term reversal faktor | napi, havi |

## Portfólió adatok

- **Size × B/M:** 6, 25, 100 portfólió
- **Size × OP:** 6, 25, 100 portfólió
- **Size × Inv:** 6, 25, 100 portfólió
- **Industry portfóliók:** 5, 10, 12, 17, 30, 38, 48, 49 iparág
- **Háromdimenziós sortolások:** size × B/M × OP, stb.

## Nemzetközi adatok

- **Fejlett piacok:** FF3 és FF5 faktorok — Europe, Japan, Asia Pacific ex-Japan, North America
- **Emerging Markets:** FF5 faktorok

## Technikai részletek

- **Formátum:** TXT és CSV
- **Időszak:** 1926–present (havi frissítés, utolsó: 2026. február)
- **Hiányzó értékek:** -99.99 vagy -999
- **Ingyenes és szabadon felhasználható**

## Kapcsolódás a rendszerhez

Ez az adatforrás nélkülözhetetlen:
- Faktor hozam time series a backtesztekhez
- Portfólió sortolás adatok a faktor validációhoz → [[methodology/factor-validation]]
- Breakpoint adatok a saját faktor portfólió konstrukcióhoz
- Nemzetközi adatok a KKE factor premium teszteléshez → [[open_questions/kke-factor-premiums]]

## Felhasználási javaslat

1. **FF5 + MOM faktor hozamok letöltése** (havi, CSV)
2. **25 size × B/M portfóliók** a modell teszteléshez (GRS teszt)
3. **Developed Europe** faktorok a KKE összehasonlításhoz
4. **Breakpoints** a saját sort implementálásához
