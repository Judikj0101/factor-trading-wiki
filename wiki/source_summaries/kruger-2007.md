---
type: source_summary
tags: [factor-model, mutual-funds, momentum]
confidence: medium
last_reviewed: 2026-04-14
related: [[entities/momentum]], [[entities/fama-french-five-factor-model]]
---

# Kruger (2007) — Persistence in Mutual Fund Performance

**Szerző:** Samuel Kruger (University of Chicago)
**Megjelenés:** June 2007 (working paper)
**Raw forrás:** `raw/papers/Mutual_Fund_Persistence.md`

## Fő állítások

1. A mutual fund teljesítmény-perzisztencia nagyrészt a **Carhart (1997) 4-factor modellel** magyarázható (Market + SMB + HML + MOM).
2. A "jó" alapkezelők nem válogatnak jobb részvényeket — a holdings returns (részvények hozama, nem az alap hozama) ugyanúgy megmagyarázhatók a 4-faktor modellel.
3. A perzisztencia fő forrása a **momentum exposure**: a nyertes alapok momentum részvényeket tartanak.
4. Az alsó decilis alulteljesítése (Carhart 1997 eredménye) **nem kapcsolódik** a részvényválasztáshoz — inkább költségek és tranzakciós díjak.

## Módszertan

- Holdings returns: a részvényeket tartják 1 évig trade nélkül → ez izolálja a stock-picking skill-t a tranzakciós döntésektől
- Decilis portfólió sortolás (Carhart módszer)
- 4-factor regresszió az alphaért

## Kapcsolódás a rendszerhez

Ez a paper megerősíti, hogy az aktív management hozzáadott értéke minimális — a "skill" valójában faktor exposure. Ez motiválja a faktor indexekbe való közvetlen befektetést (factor investing) az aktív management helyett.

## Limitációk

- Working paper, nem peer-reviewed
- US-specifikus eredmények
