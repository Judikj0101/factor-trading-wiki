---
type: source_summary
tags: [macro-factor, monetary-policy, bond-yields, emerging-markets, global, time-series]
confidence: high
last_reviewed: 2026-04-15
related: [[entities/term-premium]], [[entities/market-risk-premium]], [[concepts/monetary-policy-spillover]], [[concepts/factor-cyclicality]], [[open_questions/kke-factor-premiums]]
---

# Adrian, Gelos, Lamersdorf & Moench (2024) — Az USA monetáris politika aszimmetrikus és perzisztens hatása a globális kötvényhozamokra

**Forrás:** BIS Working Paper No. 1195, 2024. július  
**Szerzők:** Tobias Adrian (IMF), Gaston Gelos (BIS), Nora Lamersdorf (Frankfurt School), Emanuel Moench (Frankfurt School)  
**Fájl:** `raw/raw/work1195.pdf`

## Fő állítás

Az USA Fed monetáris politikai sokkjainak hatása a globális szuverén kötvényhozamokra **aszimmetrikus és tartós** — és a GFC (2008-as nagy pénzügyi válság) körül strukturális törés következett be. A mechanizmus nagy részét a befektetési alapok tőkeáramlásai (mutual fund flows) magyarázzák.

## Módszertan

- **Monetáris politikai sokk mérése:** Nakamura-Steinsson (2018) high-frequency sokkok (FOMC bejelentések körüli ±20 perc), Acosta (2022) kiterjesztésével 2022 szeptemberig.
- **Lokális projekciók (Jordà 2005):** kumulatív hozamváltozás 50 hétre előre.
- **Sokk aszimmetria:** Szigorítási vs. lazítási sokkokat külön modellezi.
- **Hozam dekompozíció:** Adrian et al. (2019) 3-faktor term structure modell → várható rövid kamat + term premium szétválasztás.
- **Panel adat:** 18 fejlett gazdaság + 15 feltörekvő piac szuverén kötvényhozamai.
- **Tőkeáramlások:** Granular szuverén kötvény befektetési alap flow adatok.

## Főbb eredmények

### Pre-GFC (1989–2007)
- **Szigorítási sokkok:** Tartós, harang alakú hozamemelkedés, csúcs ~10 héttel a bejelentés után. Az iniciális hatásnál **nagyságrenddel nagyobb** a késői hatás.
- **Lazítási sokkok:** Szinte nincs hatás a kötvényhozamokra — mert a term premium erősen emelkedett, ellensúlyozva a csökkenő kamatvárakozásokat.
- **Következmény:** A Brooks et al. (2020) által dokumentált "Post-FOMC drift" szinte kizárólag a szigorítási sokkokból ered.

### Post-GFC (2010–2021)
- **Strukturális törés:** Mind a szigorítási, mind a lazítási sokkok után a term premium tartósan csökken.
- **Szigorítási sokkokra:** Rövid kezdeti emelkedés, majd tartós hozamcsökkenés (reversal).
- **Lazítási sokkokra:** Tartós tőkebeáramlás EM és fejlett piacokra.
- **Globális spillover:** Az EM szuverén hozamok alapvetően az US Treasury dinamikáját követik, azonos aszimmetriával.

### Mechanizmus
- Az elsődleges dealer-ek mérlegének duration-váltása (negatívból pozitívba GFC körül) megmagyarázza a term premium előjelváltását, de nem a teljes képet.
- A **befektetési alapok tőkeáramlásai** (mutual fund flows) szintén perzisztensek és aszimmetrikusak — a lazítási sokkokat tartós EM/AE beáramlás követi post-GFC.

## Relevanciája a faktor trading wiki számára

**Közvetlen relevancia: magas**, különösen a KKE faktor kutatáshoz.

1. **Makro faktor:** A Fed monetáris politika sokk önálló makro faktor lehet KKE portfóliókban — különösen post-GFC, ahol a lazítási sokkokat EM tőkebeáramlás követi.
2. **Rezsimváltás:** A GFC körüli strukturális törés azt jelenti, hogy a faktor viselkedése **rezsimdependens** — pre/post-GFC mintából tanult modellek nem általánosíthatók.
3. **Term premium:** A term premium dinamikája (emelkedik lazításkor pre-GFC, csökken post-GFC) közvetlen relevanciájú KKE szuverén kötvény prémium vizsgálatoknál → lásd [[entities/term-premium]].
4. **KKE-specifikus:** A 15 EM ország mintájában KKE országok (Lengyelország, Csehország) is szerepelnek — a hozamreakció az US sokkokra az EM átlagot tükrözi.

## Limitációk

- Csak kötvénypiac — részvénypiaci faktor hatás külön tesztelendő
- Minta 2021 novemberben végződik (50 hetes előretekintési ablak miatt)
- Angol nyelvű újságok → szemiotikai lefedettség EU-ra jobb mint pl. Latin-Amerikára

## Kapcsolódó wiki oldalak

- [[entities/term-premium]] — a tanulmány alapján létrehozva
- [[concepts/monetary-policy-spillover]] — a mechanizmus részletes kifejtése
- [[concepts/factor-cyclicality]] — rezsimváltás (pre/post-GFC) mint faktor ciklusok forrása
- [[open_questions/kke-factor-premiums]] — US monetáris politika mint KKE makro faktor
