---
type: open_question
tags: [factor-model, kke, emerging-markets, cross-section]
confidence: low
last_reviewed: 2026-04-14
related: [[entities/fama-french-five-factor-model]], [[entities/smb]], [[entities/hml]], [[concepts/value-premium]], [[concepts/factor-zoo]], [[concepts/news-sentiment-factor]], [[source_summaries/foye-mramor-pahor-2016]], [[source_summaries/claesson-2021]]
---

# Mukodnek-e a Fama-French faktorok a KKE piacokon?

## A kerdes

A Fama-French faktor modellek (3-, 5-, 6-faktor) az USA piacon lettek kifejlesztve es validalva. A kelet-kozep-europai (KKE) tozsdekon — Magyarorszag, Lengyelorszag, Csehorszag, Romanis, stb. — **vajon ugyanazok a faktor premiumok leteznek, es hasonlo mertekuek?**

## Miert fontos

- Ha KKE piacokon faktor-alapu trading strategiat akarunk epiteni, tudnunk kell, **mely faktorok szignifikansak** es melyek nem.
- Az **SMB (size) faktor** gyengesege fejlodo piacokon azt jelzi, hogy a US-ben mukodo strategiak nem masolhatok egy az egyben.
- A **value premium** fenntarthatosaga vagy hianya KKE-ban kozvetlenul erinti barmely HML-alapu portfolio strategiat.
- A KKE piacok egyedi jellemzoi (likviditashiany, szamviteli minoseg, privatizacios torzitasok) eltero faktor-dinamikat hozhatnak letre.

## Amit tudunk (forrasok alapjan)

### SMB (Size) — valoszinuleg NEM mukodik

- **Foye et al. (2016):** az EE EU 8 orszagara a market value of equity faktor **gyengen teljesit** — a szerzok NI/CFO (earnings quality) proxy-val lecserlik.
- **Claesson (2021):** az aggregalt emerging market eredmenyek is azt mutatjak, hogy az SMB **redundans**.
- **Claessens et al. (1993, 1995, 1998):** mar korábban is dokumentaltak, hogy az ME gyengebb fejlodo piacokon.

### HML (Value) — valoszinuleg IGEN, de eltero mertekeben

- **Foye et al. (2016):** a HML megmarad az EE EU piacokon — a book-to-market ratio meg itt is magyaraz.
- **Claesson (2021):** a value es profitability faktorok a **fo hozamhajtok** fejlodo piacokon.
- **Fama & French (1998):** globalis dataset-en is megerositik a value premiumot fejlodo piacokon.

### RMW (Profitability) — valoszinuleg IGEN

- **Claesson (2021):** a profitability faktor szignifikans fejlodo piacokon.
- KKE-specifikus teszt nem ismert — de az earnings quality relevanciajabol (Foye et al.) kovetkeztetheto.

### CMA (Investment) — valoszinuleg NEM

- **Claesson (2021):** redundans fejlodo piacokon.
- KKE-specifikus adat nincs.

### Momentum — nincs meggyozo evidencia

- **Claesson (2021):** a hatfaktoros modell (momentum hozzadasaval) **insignifikans** fejlodo piacokon.

### Earnings Quality (NI/CFO) — potencialis KKE-specifikus faktor

- **Foye et al. (2016):** a szamviteli manipulacio proxy (NI/CFO) **szignifikansan jobb** mint az SMB az EE EU piacokon.
- Ez egy a [[concepts/factor-zoo]] bővitmeny, ami KKE-ban relev lehetáns.

## Amit NEM tudunk

1. **Friss adatok:** a Foye et al. tanulmany 2005–2010, Claesson 2021-ig — de nincs KKE-specifikus friss elemzes.
2. **Magyarorszag-specifikus eredmenyek:** egyetlen tanulmany sem ad Magyarorszag-onallo bontast.
3. **Faktor premiumok nagysaga:** ha a value premium letezik is KKE-ban, **mekkora** es mennyire stabil?
4. **Sentiment faktor KKE-ban:** a [[concepts/news-sentiment-factor]] tesztelese KKE piacokra nem tortent meg.
5. **Rezsimuerzekenyueg:** a KKE piacok 2004 (EU csatlakozas), 2008 (valsag), 2020 (COVID) korul nagyon kulonbozo rezsimuekben mukodtek — az allando faktor premiumok feltételezése kerdéses.

## Milyen forrasra lenne szukseg

- **KKE-specifikus faktor study** friss adatokkal (2015–2025), reszveny-szintu cross-section-nel.
- **Out-of-sample teszt:** ha van US-ben mukodo faktor, tesztelni KKE-ban (es forditva).
- **GDELT-alapu sentiment teszt** KKE indexekre (BUX, WIG20, PX) — osszekotes a [[entities/gdelt]] es factor trading kozott.
- **Likviditasi kontroll:** a KKE piacok illikviditasa torzithatja a faktor premiumokat.

## Erintett wiki oldalak

- [[entities/fama-french-five-factor-model]]
- [[entities/smb]]
- [[entities/hml]]
- [[concepts/value-premium]]
- [[concepts/factor-zoo]]
- [[concepts/news-sentiment-factor]]
- [[entities/gdelt]]
