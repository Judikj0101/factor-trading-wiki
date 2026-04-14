---
type: entity
tags: [factor-model, cross-section, momentum]
confidence: high
last_reviewed: 2026-04-14
related: [[entities/fama-french-five-factor-model]], [[entities/smb]], [[entities/hml]], [[source_summaries/msci-foundations-2013]], [[concepts/factor-cyclicality]]
---

# Momentum faktor

## Definíció

Részvények amelyek az elmúlt 3–12 hónapban felülteljesítettek, hajlamosak a következő hónapban is felülteljesíteni (és fordítva). A momentum faktor ezt a mintázatot ragadja meg long-short portfólióval.

$$MOM_t = R_{winners,t} - R_{losers,t}$$

Szokásos mérőszám: elmúlt 12 havi hozam, az utolsó 1 hónap kizárásával (12-2 momentum).

## Helye a faktor modellekben

- **Nem része az FF5 modellnek** — Fama & French (2014) szándékosan kihagyta
- **Carhart (1997):** FF3 + MOM = 4-faktor modell
- **MSCI:** a hat risk premia faktor egyike
- A momentum az egyetlen faktor amit Fama & French nem tartanak kockázati kompenzációnak

## Prémium magyarázatok

| Megközelítés | Magyarázat |
|---|---|
| Risk-based | Magasabb tail risk, üzleti ciklus érzékenység |
| Behavioral | Underreaction (lassú információ-feldolgozás), overreaction (trend-following), herding |
| Institutional | Reputation-driven herding (Dasgupta, Prat & Verardo 2011) |

## Jellemzők

- Az egyik legmagasabb Sharpe-rátájú faktor hosszú távon
- **Rendkívül ciklikus** — momentum crash-ek (pl. 2009 Q1) nagyon súlyosak
- Magas turnover → magasabb tranzakciós költségek
- Rövid távú (1 hónap) reversal és hosszú távú (3–5 év) reversal is dokumentált

## Források

- [[source_summaries/carhart-1997]]
- [[source_summaries/msci-foundations-2013]]
