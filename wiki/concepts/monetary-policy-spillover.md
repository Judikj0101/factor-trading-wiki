---
type: concept
tags: [macro-factor, monetary-policy, emerging-markets, kke, global, time-series, regime]
confidence: high
last_reviewed: 2026-04-15
related: [[entities/term-premium]], [[entities/market-risk-premium]], [[concepts/factor-cyclicality]], [[open_questions/kke-factor-premiums]], [[source_summaries/adrian-gelos-lamersdorf-moench-2024]], [[source_summaries/arteta-kamin-ruch-2022]]
---

# Monetáris politikai spillover

## Mi ez

Az USA Fed monetáris politikai döntéseinek hatása más — különösen feltörekvő — piacokra. A spillover azért jön létre, mert:
- A dollár globális tartalékvaluta → USD kamatszint befolyásolja a globális hitelfeltételeket
- A befektetők globálisan allokálnak → Fed szigorítás tőkekivonást okoz az EM-ekből
- Az EM szuverén adósság döntő része USD-ben van denominálva → a kamatemelés közvetlenül drágítja az adósságszolgálatot

## A sokkdekompozíciós keretrendszer (Arteta et al. 2022)

Az USA kamatszint-változás három típusú sokkból állhat, amelyek **gyökeresen eltérő EMDE-hatást** eredményeznek:

### Reál sokk
- **Azonosítás:** ↑ US hozam + ↑ részvény + ↑ inflációs várakozás
- **Értelmezés:** Az USA gazdasági aktivitás erősödése hajtja a kamatszint-emelkedést
- **EMDE hatás:** Kedvező — a US import-kereslet nő, befektetői hangulat javul, tőkebeáramlás az EM-ekbe

### Inflációs sokk
- **Azonosítás:** ↑ US hozam + ↓ részvény + ↑ inflációs várakozás
- **Értelmezés:** Magasabb inflációs várakozások hajtják a hozamokat
- **EMDE hatás:** Káros — magasabb finanszírozási költségek, devizaleértékelés, tőkebeáramlás csökkenés

### Reakciós sokk
- **Azonosítás:** ↑ US hozam + ↓ részvény + ↓ inflációs várakozás
- **Értelmezés:** A piac úgy értékeli, hogy a Fed hawkisabbá válik (policy stance váltás)
- **EMDE hatás:** Legsúlyosabb — szuverén spread szélesedés, devizaválság kockázat csaknem megduplázódik

## Perzisztencia és aszimmetria (Adrian et al. 2024)

A Fed sokkokra adott globális kötvénypiaci reakció:
- **Tartós:** az iniciális hatásnál nagyságrenddel nagyobb a 10 hetes kumulatív hatás
- **Aszimmetrikus:** szigorítás és lazítás különböző irányú és nagyságú hatást vált ki
- **Rezsimdependens:** a GFC (2008) strukturális törést hozott — pre/post-GFC viselkedés alapvetően eltér

### Post-GFC EM viselkedés
- Lazítási sokkokra: tartós tőkebeáramlás EM-ekbe, hozamcsökkentés
- Szigorítási sokkokra: rövid hozamemelkedés, majd reversal (hozamcsökkentés) a term premium esés miatt
- **Következmény:** a post-GFC időszakban a Fed tightening kevésbé tartósan emeli az EM hozamokat, mint korábban

## Faktor trading következmények

### Makro faktor alkalmazás
A Fed sokktípusa beépíthető KKE részvényfaktor modellbe kontrollváltozóként:
- **Reakciós sokk rezsimben:** risk-off → value prémium emelkedik (defensive), momentum összeomlik, quality defensív irányba mozog
- **Reál sokk rezsimben:** risk-on → growth/momentum faktorok dominálnak, EM equity felülteljesít

### Rezsimdetekció
A VAR-alapú sokkdekompozíció alkalmazható valós idejű rezsimdetekciós jelként:
- Inputok: 2Y US hozam változás, S&P 500 változás, breakeven inflációs várakozás változás
- Output: valószínűségi súlyok a három sokkregzsim között
- Felhasználás: faktor-allokáció dinamikus súlyozása a rezsim függvényében

### KKE-specifikus
- KKE piacok (BUX, WIG20, PX) reakciós sokkokra különösen érzékenyek → magas geopolitikai kockázat + gyenge deviza + szuverén prémium kombináció
- Az EU-tagság (tőkeáramlási integráció) felerősíti a spillover csatornát
- Lásd: [[open_questions/kke-factor-premiums]]

## Nyitott kérdések

1. A sokkdekompozíciós jel mennyire működik valós idejű rezsimdetekciós célra (look-ahead bias)?
2. KKE-specifikus sokkérzékenység különbözik-e az általános EM-től?
3. Hogyan interaktál a US monetáris politikai sokk a helyi KKE jegybanki politikával (NBP, MNB, CNB)?
4. Alkalmazható-e a term premium változása KKE részvény-szelekciós faktorként?

## Kapcsolódó oldalak

- [[entities/term-premium]] — a kötvényhozam term premium komponense
- [[entities/market-risk-premium]] — részvénykockázati prémium analógiája
- [[concepts/factor-cyclicality]] — monetáris rezsimek és faktor ciklusok
- [[source_summaries/adrian-gelos-lamersdorf-moench-2024]] — perzisztencia és aszimmetria
- [[source_summaries/arteta-kamin-ruch-2022]] — sokkdekompozíció és EMDE hatások
