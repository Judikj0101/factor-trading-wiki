---
type: source_summary
tags: [factor-model, kke, emerging-markets, cross-section, earnings-quality]
confidence: medium
last_reviewed: 2026-04-14
related: [[entities/fama-french-five-factor-model]], [[entities/smb]], [[entities/hml]], [[concepts/value-premium]], [[open_questions/kke-factor-premiums]]
---

# Foye, Mramor & Pahor (2016) — A Respecified Fama French Three Factor Model for the Eastern European Transition Nations

## Bibliograia

- **Szerzok:** James Foye, Dusan Mramor, Marko Pahor
- **Intézmeny:** University of Ljubljana, Faculty of Economics
- **Ev:** 2016
- **SSRN:** 2742170
- **Forras fajl:** `raw/papers/ssrn_id2742170_code1714688.md`

## Fo allitasok

1. A klasszikus Fama-French 3-faktoros modell **rosszul teljesit** a 2004-ben EU-hoz csatlakozott kelet-europai (EE EU) orszagokban: **Csehorszag, Eszorszag, Magyarorszag, Lettorszag, Litvania, Lengyelorszag, Szlovakia, Szlovenia**.
2. A **market value of equity (ME / size) komponens** kulonosen gyengen magyarazza a hozamokat ezeken a piacokon — osszhangban mas fejlodo piaci tanulmanyokkal.
3. A szerzok **uj modellt javasolnak**: a size faktort lecserlik egy **earnings quality proxy-ra** (NI/CFO — net income / cash from operations), ami a szamviteli manipulacio meroszama.
4. A **modositott modell szignifikansan jobb magyarazo erot** mutat az EE EU piacokra, mint az eredeti FF3.
5. Az **earnings management** szintje magas a kelet-europai tranziciós orszagokban — a szamviteli standardok atallasa (legisztikus → IFRS) torzitasokat okoz.

## Kulcs mechanizmus

Az EE EU piacok jellegzetessegei:
- **Gyenge intezmenyi hatter:** a privatizacio meg folyamatban van, a szamviteli szabalyok ujak.
- **Earnings manipulation:** a NI/CFO arany magas, mert a cegek agressziven menedzselik az eredmenyt (kulonosen a 0 korul — cegek felfelé tolják az eredmenyt).
- **Accounting quality > Size:** a befektetok nem a cegmeretet, hanem a szamviteli minoseg szintjet arazak be.

## Relevans eredmenyek a factor trading rendszerhez

- **Kozvetlen KKE relevancia:** ez az egyetlen forrasunk, ami specifikusan a kelet-europai EU-tagallamokra tesztel faktor modelleket.
- **SMB nem mukodik KKE-ban** — ez egy fontos jelzes barmilyen KKE faktor strategia tervezesehez.
- **HML (value) megmarad** — a book-to-market ratio meg ezeken a piacokon is magyaraz.
- **Earnings quality faktor** potencialisan hasznos KKE-ban — ez a [[concepts/factor-zoo]] egy erdekes KKE-specifikus bovitmeny.
- Az idohorizont rovid (2005–2010) es heti adatokat hasznal a havi helyett — a statisztikai robusztuság korlátozott.

## Limitaciok

- **Rovid idoszak:** 2005. julius – 2010. junius (5 ev).
- **Heti hozamok** a havi helyett (nem standard metodologia).
- **Kis mintameret:** a Stoxx EU Enlarged Total Market Index alkotoi, de sok reszveny kizarva.
- Nem teszteli az otfaktoros vagy hatfaktoros modellt.
- Bulgária, Ciprus, Malta, Romania kizarva — csak a 2004-es csatlakozok.
