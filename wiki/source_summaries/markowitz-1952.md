---
type: source_summary
tags: [portfolio, risk-management, statistics]
confidence: high
last_reviewed: 2026-04-14
related: [[concepts/covariance-matrix]], [[entities/sharpe-ratio]], [[entities/capm]], [[entities/barra-risk-model]]
---

# Markowitz (1952) — Portfolio Selection

**Szerző:** Harry M. Markowitz
**Megjelenés:** 1952, The Journal of Finance, Vol. VII, No. 1, 77–91
**Raw forrás:** `raw/papers/Markowitz1952.pdf` (scanned, szöveg nem kinyerhető)

## Fő állítások

1. A portfólió-választás nem egyszerűen a legmagasabb várható hozamú részvény kiválasztása — a **diverzifikáció** csökkenti a kockázatot.
2. A befektető célja: adott kockázati szint mellett a legmagasabb várható hozam, vagy adott hozam mellett a legalacsonyabb kockázat → **mean-variance optimalizálás**.
3. Az **efficient frontier** (hatékony határvonal) azokat a portfóliókat tartalmazza, amelyeknél nem lehet javítani az egyik dimenzión (hozam/kockázat) a másik romlása nélkül.
4. A portfólió kockázata nem az egyedi részvények kockázatainak összege, hanem a **kovarianciák** függvénye:

$$\sigma_p^2 = \sum_i \sum_j w_i w_j \sigma_{ij}$$

## Hatás

- A **Modern Portfolio Theory (MPT)** alapja — a kvantitatív portfólió management innen indul
- Minden multi-factor kockázati modell (Barra, stb.) erre épít → [[entities/barra-risk-model]]
- A kovariancia mátrix becslése a gyakorlati kihívás → [[concepts/covariance-matrix]]
- Sharpe (1964) a CAPM-et ebből a keretből vezeti le → [[entities/capm]]
- Markowitz 1990-ben Nobel-díjat kapott

## Kapcsolódás a rendszerhez

A Markowitz-féle mean-variance keretrendszer a factor investing alapja: a faktor modellek a kovariancia mátrix struktúrált becslését adják, ami a portfólió optimalizálás inputja.
