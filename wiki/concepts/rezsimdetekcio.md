---
type: concept
tags: [regime, factor-cyclicality, time-series, macro-factor, kke, methodology]
confidence: medium
last_reviewed: 2026-04-15
related: [[concepts/factor-cyclicality]], [[concepts/monetary-policy-spillover]], [[entities/term-premium]], [[open_questions/kke-factor-premiums]], [[source_summaries/ang-bekaert-2002]], [[source_summaries/adrian-gelos-lamersdorf-moench-2024]], [[source_summaries/arteta-kamin-ruch-2022]]
---

# Rezsimdetekció (Regime Detection)

## Mi ez

A pénzügyi piacok időben **nem homogének** — különböző időszakokban eltérő hozam-, volatilitás- és korreláció-dinamika jellemzi őket. A rezsimdetekció célja ezeknek a **diszkrét vagy folytonos állapotváltásoknak az azonosítása** valós időben vagy utólag.

## Miért fontos faktor trading szempontból

- A faktorprémiumok **rezsimdependensek**: value 2010–2020 között alulteljesített (növekedési rezsim), momentum összeomlik válságban (korreláció-törés)
- Különböző rezsimdekben **különböző optimális faktor-allokáció** érvényes
- A KKE piacok rezsimváltásai (EU-csatlakozás 2004, pénzügyi válság 2008, COVID 2020, Ukrajna 2022) fundamentálisan eltérő faktordinamikát eredményezhetnek

## Főbb rezsimdetekciós módszerek

### 1. Markov Regime Switching (MRS) modell — Ang & Bekaert (2002)

A legszélesebb körben alkalmazott empirikus módszer:

$$R_t = \mu_{s_t} + \Sigma_{s_t}^{1/2} \epsilon_t$$

ahol $s_t \in \{1, 2, ..., K\}$ a látens rezsimváltozó, $P(s_{t+1}=j | s_t=i) = p_{ij}$ az átmeneti valószínűség.

- **Előny:** Explicit valószínűséget ad minden rezsimre, kezeli az aszimmetrikus korrelációkat
- **Alkalmazás:** Ang & Bekaert (2002) 2 rezsimmel (normál + medve) — a medve rezsimben magasabb korreláció, alacsonyabb hozam
- **Becslésmódszer:** EM-algoritmus (Expectation-Maximization) vagy Hamilton-szűrő

### 2. VAR-alapú sokkdekompozíció — Arteta et al. (2022)

A monetáris politikai sokkokat háromféle rezsimbe sorolja jel-restrikciók alapján:
- **Reál sokk rezsim** → pozitív EM részvény
- **Inflációs sokk rezsim** → negatív EM részvény
- **Reakciós sokk rezsim** → legsúlyosabb EM drawdown

Lásd részletesen: [[concepts/monetary-policy-spillover]]

### 3. Strukturális törés tesztek

- **Chow-teszt:** egyszerű törés egy előre megadott időpontban
- **Bai-Perron teszt:** endogén töréspontok azonosítása
- **Zivot-Andrews:** törésponttal kiegészített egységgyök-teszt
- **Alkalmazás:** GFC előtt/után strukturális törés a Fed sokkok hatásában (Adrian et al. 2024)

### 4. Rolling/expanding window elemzés

- Egyszerűbb, de kevésbé formális — faktor prémiumok időben változó becslése

## Rezsimindikátor változók (inputs)

| Változó | Mit jelez | Forrás |
|---|---|---|
| GPR index | Geopolitikai kockázat szint | [[entities/gpr-index]] |
| Term premium | Hozamgörbe laposodása | [[entities/term-premium]] |
| Credit spread | Hitelkockázati prémium | — |
| VIX | Részvénypiaci implált volatilitás | — |
| Fed sokktípus | Reál / Infláció / Reakció | [[concepts/monetary-policy-spillover]] |
| GDELT Tone | Médiasentiment | [[entities/gdelt]] |

## KKE-specifikus rezsimek

A KKE piacok historikusan azonosítható rezsimváltásai:

| Esemény | Hatás |
|---|---|
| EU-csatlakozás (2004) | Tőkebeáramlás, integráció mélyülése |
| Globális pénzügyi válság (2008) | Korrelációk emelkedtek, minden faktor esett |
| Európai adósságválság (2011–12) | KKE devizák gyengülése |
| COVID (2020) | Éles, rövid drawdown + V-alakú visszapattanás |
| Orosz invázió (2022.02) | GPR csúcs, tőkekivonás, különösen BUX érintett |

**Kutatási gap:** A KKE specifikus rezsimek és a faktorprémiumok kapcsolatának szisztematikus vizsgálata **hiányzik** — lásd [[open_questions/kke-factor-premiums]]

## Nyitott kérdések

1. Az MRS modell mennyire alkalmas valós idejű rezsimdetekciókra KKE részvényadatokon (kis minta)?
2. A GPR alindex (GPT vs. GPA) melyike jobb rezsimindikátor KKE piacokon?
3. A KKE EU-csatlakozás (2004) strukturális törést okoz-e a faktorprémiumokban?
4. Milyen frekvencián kell a rezsimet újrabecsülni egy dinamikus faktor-allokációs rendszerben?

## Kapcsolódó wiki oldalak

- [[concepts/factor-cyclicality]] — a rezsimváltás és a faktor ciklusok kapcsolata
- [[concepts/monetary-policy-spillover]] — Fed sokkdekompozíció mint rezsimindikátor
- [[source_summaries/ang-bekaert-2002]] — MRS modell empirikus alkalmazása
- [[entities/gpr-index]] — geopolitikai rezsimindikátor
- [[entities/term-premium]] — hozamgörbe-alapú rezsimindikátor
