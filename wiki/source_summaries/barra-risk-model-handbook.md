---
type: source_summary
tags: [risk-management, factor-model, regression, portfolio]
confidence: high
last_reviewed: 2026-04-14
related: [[entities/barra-risk-model]], [[entities/fama-french-five-factor-model]], [[concepts/covariance-matrix]]
---

# Barra Risk Model Handbook (2007)

**Kiadó:** MSCI Barra
**Megjelenés:** 2007 (RV 10-2007)
**Raw forrás:** `raw/standards/barra_risk_model_handbook.md`

## Fő tartalom

Átfogó kézikönyv a Barra multi-factor kockázati modellekről. Lefedi:

1. **Multiple-Factor Models (MFM) elmélete** — hogyan bontják szét a portfólió kockázatát common és specific komponensekre
2. **Equity risk modeling** — fundamentális faktor modellek (Barra USE sorozat)
3. **Fixed-income risk modeling** — kamatláb és spread kockázat
4. **Currency risk modeling** — devizakockázat
5. **Integrated risk modeling** — multi-asset class kockázati modell (BIM)

## Kulcs koncepciók

### A Barra MFM keretrendszer
- **Faktor típusok:** fundamentális (industry, style), makroökonómiai, statisztikai
- **Faktor hozam becslés:** cross-sectional regresszió (nem portfólió sort mint FF)
- **Kovariancia mátrix:** exponenciális súlyozás, volatility scaling
- **Specific risk:** az a rész amit a faktorok nem magyaráznak

### A Barra vs Fama-French megközelítés
| Aspektus | Barra | Fama-French |
|---|---|---|
| Faktor hozam becslés | Cross-sectional regresszió | Portfólió sortolás (long-short) |
| Cél | Kockázat előrejelzés | Asset pricing, anomáliák tesztelése |
| Frissítés | Napi | Havi |
| Faktorok száma | ~60+ (industry + style) | 3–5 |

### Modell evolúció
- USE1 (1975) → USE2 (1985) → USE3 (1997) → USE4 (2011)
- GEM (1989) → GEM2 (2008) → GEMLT

## Limitációk

- Proprietáris modell — részletes adatok és kód nem publikus
- A handbook inkább általános áttekintés, a technikai részletek a USE4 Methodology Notes-ban vannak

## Kapcsolódás a rendszerhez

A Barra modell az ipari standard a portfólió kockázat mérésére. A factor investing szempontjából a Barra faktorok és az FF faktorok összevetése fontos — ugyanazt mérik, de más módszertannal.

## Hivatkozott könyvek

- Grinold & Kahn: *Active Portfolio Management* (1995, 2000)
- Rudd & Clasing: *Modern Portfolio Theory* (1988)
