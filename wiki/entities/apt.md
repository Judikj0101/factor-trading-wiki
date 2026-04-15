---
type: entity
tags: [factor-model, theory, capm, apt, cross-section]
confidence: high
last_reviewed: 2026-04-15
related: [[entities/capm]], [[entities/fama-french-five-factor-model]], [[entities/barra-risk-model]], [[source_summaries/ross-1976]]
---

# APT — Arbitrage Pricing Theory

## Definíció

A **Ross (1976)** által bevezetett multifaktoros eszközárazási elmélet. A CAPM egyfaktoros modelljével szemben az APT szerint a várható hozamot **több szisztematikus kockázati faktor** határozza meg, amelyekért a befektetők prémiumot kapnak.

## Az APT egyenlete

Ha a hozamok faktormódellel írhatók le:

$$R_i = E_i + \sum_{k=1}^K \beta_{ik} \delta_k + \epsilon_i$$

Ahol:
- $\delta_k$: a $k$-adik közös faktor meglepetés-komponense (mean zero)
- $\beta_{ik}$: az $i$-edik eszköz $k$-adik faktorra vonatkozó terhelése (loading)
- $\epsilon_i$: idiosynkratikus zaj (nagy portfólióban diverzifikálható)

Akkor **no-arbitrage feltétel** mellett:

$$E[R_i] = R_f + \sum_{k=1}^K \beta_{ik} \lambda_k$$

Ahol $\lambda_k$ az egységnyi $k$-faktorkitettségért járó kockázati prémium.

## Különbség a CAPM-tól

| Dimenzió | CAPM | APT |
|---|---|---|
| Faktorok száma | 1 (piaci portfólió) | K (tetszőleges) |
| Feltételezések | Normális hozam VAGY quadratikus preferencia | Nincs ilyen szükség |
| Piaci portfólió | Szükséges azonosítani | Nem szükséges |
| Pontosság | Exact (egyensúlyi) | Közelítő (arbitrázs-alapú) |
| Faktorok tartalma | Specifikált ($R_M - R_F$) | **Nem specifikált** |

## A faktorok azonosításának problémája

Az APT **nem mondja meg, melyek a faktorok**. Empirikus megközelítések:

1. **Statisztikai faktorok:** PCA, faktoranalízis a hozamkovariancia-mátrixon
2. **Makrogazdasági faktorok:** Chen, Roll & Ross (1986) — ipari termelés, infláció, hozamgörbe stb.
3. **Fundamental faktorok:** Fama-French — size, value, profitability, investment
4. **Barra:** Iparági és stílushatások kombinációja

## Jelentősége

- Az **összes modern multifaktoros modell elméleti alapja**
- A Barra modell [[entities/barra-risk-model]] és a Fama-French modellek [[entities/fama-french-five-factor-model]] az APT kereteiben értelmezhetők
- Az APT megindokolja, hogy KKE-specifikus kockázati tényezők (geopolitikai kockázat, likviditás, átmeneti gazdaság prémium) legitim extra faktorok lehetnek

## Limitációk

- A faktorok száma és tartalma empirikusan határozandó meg — nincs elméleti útmutatás
- Csak közelítő árképzést ad (nem exact): kis portfóliókban arbitrázs-reziduum marad
- A prémiumok ($\lambda_k$) időben változhatnak

## Kapcsolódó oldalak

- [[entities/capm]] — az APT alternatívája
- [[entities/fama-french-five-factor-model]] — az APT egy empirikus megvalósítása
- [[entities/barra-risk-model]] — Barra multifaktor modell (APT keretben)
- [[source_summaries/ross-1976]] — az eredeti paper
