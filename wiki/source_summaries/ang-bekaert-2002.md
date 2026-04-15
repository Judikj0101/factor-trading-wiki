---
type: source_summary
tags: [regime, international, portfolio, correlation, kke, emerging-markets, factor-cyclicality]
confidence: high
last_reviewed: 2026-04-15
related: [[concepts/rezsimdetekcio]], [[concepts/factor-cyclicality]], [[concepts/monetary-policy-spillover]], [[open_questions/kke-factor-premiums]]
---

# Ang & Bekaert (2002) — International Asset Allocation With Regime Shifts

**Forrás:** Review of Financial Studies, 15(4), 1137–1187, 2002  
**Szerzők:** Andrew Ang, Geert Bekaert (Columbia University + NBER)  
**Fájl:** `raw/raw/1137.pdf`

## Fő állítás

A nemzetközi részvénypiacok **korreláció- és volatilitás-dinamikája rezsimfüggő**: "normál" rezsimben alacsony korreláció és volatilitás, "medve" rezsimben magasabb korreláció, magasabb volatilitás és alacsonyabb várható hozam. Az **optimális portfólió-allokáció figyelembe veszi ezt a rezsimváltást**, és a nemzetközi diverzifikáció értékes marad rezsimváltások ellenére is.

## A modell

**Rezsimváltó (Markov Regime Switching) modell:**
- Két diszkrét rezsim: $s_t \in \{1, 2\}$ (normál és medve)
- Minden rezsimben különböző várható hozam, volatilitás és korrelációmátrix
- A rezsim átmeneti valószínűségei:
$$P(s_{t+1} = j | s_t = i) = p_{ij}$$
- A befektető nem figyeli közvetlenül a rezsimet — szűrővel becsli a valószínűségét

**Dinamikus portfólió optimalizálás:**
- CRRA (izoelasztikus) hasznossági függvény
- Havi újraegyensúlyozás
- Numerikus megoldás (backward induction)

## Főbb eredmények

1. **Medve rezsim korrelációk:** A feltételezett korrelációk szignifikánsan magasabbak a medve rezsimben — éppen akkor, amikor a diverzifikáció a leginkább kellene.
2. **Diverzifikáció értéke fennmarad:** A rezsimváltás ellenére a **nemzetközi diverzifikáció jelentős utility gainnel jár** — a home bias stratégia szub-optimális.
3. **Rezsim ignorálásának költsége:** A rezsimváltás figyelmen kívül hagyása kis hasznossági veszteséggel jár all-equity portfóliókban, de **nagyobb veszteséggel**, ha kockázatmentes eszköz is tartható.
4. **Devizahedging:** Az árfolyamkockázat fedezése rezsimváltó környezetben is értékes — külön utility gain mérhető.
5. **Befektetési horizont:** A rezsimváltás hatása **horizont-dependens** — hosszabb horizontú befektetőknek más az optimális allokáció.

## A módszertan újdonsága

- Kombinált **rezsimváltás + kamatlábak által prediktált várható hozamok** DGP
- A statisztikai szignifikancia tesztelésére delta-módszer alkalmazása klasszikus ökonometriai keretben (nem Bayes)
- Intertemporal hedging demands formális tesztje

## Relevanciája a wiki számára

**Közvetlen relevanciája: magas** a rezsimdetekció és KKE faktor kutatáshoz.

1. **Rezsimdetekció elméleti alapja:** Az Ang & Bekaert modell az egyik legelterjedtebb keretrendszer a rezsimváltás empirikus azonosítására pénzügyi piacokon → [[concepts/rezsimdetekcio]]
2. **KKE korreláció dinamika:** A KKE piacok (BUX, WIG20, PX) és a global/EU piacok korrelációja valószínűleg szintén rezsimfüggő — medve rezsimben (pl. 2008, 2022) a korrelációk emelkednek, csökkentve a diverzifikációs értéket
3. **Faktor ciklikusság:** A rezsimváltás magyarázza a faktorok ciklikus alulteljesítését — [[concepts/factor-cyclicality]]
4. **Monetáris politika spillover kapcsolat:** Az Ang-Bekaert medve rezsim nagymértékben átfed az Adrian et al. (2024) "reakciós sokk" periódusaival

## Limitációk

- US-centrikus befektető perspektíva
- Csak fejlett piacok (USA, UK, Németország) az eredeti specifikációban — KKE nem szerepel közvetlenül
- A rezsimek száma exogén (2 rezsim) — a valóság több rezsimet is tartalmazhat

## Kapcsolódó wiki oldalak

- [[concepts/rezsimdetekcio]] — az Ang-Bekaert modell alkalmazása faktor trading kontextusban
- [[concepts/factor-cyclicality]] — rezsimváltás mint a faktor ciklikusság forrása
- [[concepts/monetary-policy-spillover]] — a medve rezsim és a reakciós Fed sokkok kapcsolata
- [[open_questions/kke-factor-premiums]] — KKE korreláció dinamika és diverzifikáció
