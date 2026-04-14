---
type: source_summary
tags: [factor-model, momentum, mutual-funds, cross-section]
confidence: high
last_reviewed: 2026-04-14
related: [[entities/carhart-four-factor-model]], [[entities/momentum]], [[entities/fama-french-five-factor-model]], [[entities/alpha]], [[source_summaries/kruger-2007]]
---

# Carhart (1997) — On Persistence in Mutual Fund Performance

**Szerző:** Mark M. Carhart
**Megjelenés:** 1997, Journal of Finance, Vol. 52, No. 1, 57–82
**Raw forrás:** `raw/papers/Carhart1997.md` (JSTOR verzió, szöveg kinyerve)

## Fő állítások

1. A mutual fund teljesítmény **perzisztenciája** nagyrészt négy faktorral magyarázható: market, size, value, és **momentum**.
2. A **négyfaktoros modell** (FF3 + MOM) bevezetése:
$$R_{it} - R_{Ft} = \alpha_i + b_i(R_{Mt} - R_{Ft}) + s_i \cdot SMB_t + h_i \cdot HML_t + m_i \cdot PR1YR_t + e_{it}$$
3. Az alsó decilis alapok (worst past performers) tartósan alulteljesítenek — de ez nagyrészt **költségek és tranzakciós díjak**, nem negatív stock-picking skill.
4. A felső decilis alapok rövid távú felülteljesítése nagyrészt **momentum exposure** — nem valódi alpha.
5. **Egyéves momentum faktor (PR1YR):** a múlt évi nyertesek − vesztesek hozama. Ez a Jegadeesh & Titman (1993) momentum hatásának faktor-mimicking portfóliója.

## A négyfaktoros modell (Carhart 4F)

| Faktor | Konstrukció |
|---|---|
| $R_M - R_F$ | Piaci excess return |
| SMB | Fama-French (1993) size faktor |
| HML | Fama-French (1993) value faktor |
| PR1YR (MOM) | Nyertesek − vesztesek: top 30% − bottom 30% based on prior 12-month return (utolsó hónap kizárva) |

## Fő eredmények

- **Decilis portfóliók:** alapokat múlt évi hozam alapján 10 csoportba sorolva, évente újrasortolva
- Az 1. (legrosszabb) decilis: szignifikáns negatív alpha még a 4-factor modellben is → de ez a magas expense ratio és turnover miatt van
- A 10. (legjobb) decilis: rövid távú alpha alig szignifikáns, és a momentum faktor felszívja
- **"Do not chase winners"** — a perzisztencia illúzió, amit a momentum exposure és a költségek magyaráznak

## Részletes eredmények (a teljes szövegből)

- **Survivor bias-free minta:** 1962–1993, diversified equity funds — korábbi tanulmányok hibáját javítja
- **"Hot hands" = momentum exposure:** Hendricks, Patel & Zeckhauser (1993) eredménye a Jegadeesh-Titman momentum hatásból fakad
- **Momentum stratégia nem működik fund szinten:** alapok amelyek momentum részvényeket tartanak, nem a stratégia tudatos követése miatt tartják — véletlenül kerülnek az adott részvényekbe
- **Tranzakciós költségek:** ~0.95% per trade market value — a momentum stratégia nyereségét felemészti
- **Expense ratio hatása:** legalább 1:1 negatív hatás a teljesítményre
- **Load funds:** expense ratio-n felül ~80 bp/év alulteljesítés (a load díjakat nem is számítva)
- **Legjobb decilis:** a jövőbeli alpha statisztikailag nem szignifikáns — legfeljebb visszakeresik a költségeiket

## Hatás az irodalomra

- A Carhart 4F lett a **de facto standard** a mutual fund teljesítmény értékeléséhez
- A momentum faktor bekerült a mainstream factor modellezésbe
- Fama & French (2014) az FF5-ben **szándékosan kihagyták** a momentumot — nem tekintik kockázati faktornak, hanem behavioral anomáliának

## Kapcsolódás a rendszerhez

- A Carhart modell a fund/stratégia alpha mérés standardja
- A momentum faktor az egyik legerősebb és legciklikusabb anomália → [[entities/momentum]], [[concepts/factor-cyclicality]]
- Kruger (2007) a Carhart eredményeket holdings returns-szel megerősíti → [[source_summaries/kruger-2007]]
