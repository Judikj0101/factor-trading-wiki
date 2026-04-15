---
type: source_summary
tags: [factor-model, cross-section, value, size, capm, statistics]
confidence: high
last_reviewed: 2026-04-15
related: [[entities/hml]], [[entities/smb]], [[entities/capm]], [[entities/fama-french-five-factor-model]], [[source_summaries/fama-french-1993]], [[source_summaries/fama-french-2014]]
---

# Fama & French (1992) — The Cross-Section of Expected Stock Returns

**Forrás:** Journal of Finance, 47(2), 427–465, 1992  
**Szerzők:** Eugene F. Fama, Kenneth R. French  
**Fájl:** `raw/raw/the_cross-section_of_expected_stock_returns.pdf` (scanned)

## Fő állítás

A CAPM béta **nem magyarázza** a részvényhozamok keresztmetszetét, ha a méret (market equity, ME) kontrollálva van. Ezzel szemben a **méret (ME)** és a **könyv szerinti érték / piaci érték arány (BE/ME)** együttesen lefedi az összes szisztematikus kockázatot a részvényhozamokban.

## Módszertan

- **Adatok:** NYSE, AMEX, NASDAQ részvények, 1963–1990
- **Fama-MacBeth regresszió:** Havi keresztmetszeti regressziók, átlagolt koefficiensek
- **Portfólió sorba rendezés:** Méret és BE/ME szerint quintile-ok
- **Bétabecslés:** Portfóliók bétáját becslik, majd egyedi részvényekhez rendelik (EIV-probléma csökkentése)

## Főbb eredmények

1. **Béta halott:** A CAPM béta és a hozam közötti kapcsolat **eltűnik**, ha méret kontrollálva van. A béta önmagában nem magyarázza a várható hozamot.
2. **Méret (ME) prémium:** Kisebb cégek magasabb hozamot termelnek — negatív kapcsolat log(ME) és várható hozam között. A size prémium ~0.15%/hó (3× erősebb, mint gondolták).
3. **Value prémium (BE/ME):** Magas BE/ME (value) részvények szignifikánsan felülteljesítenek. Legerősebb hatás a Fama-MacBeth regresszióban.
4. **Kombinált modell:** Méret + BE/ME kétváltozós modell lefedi a béta, kockázat és hozam közötti kapcsolatot.
5. **E/P, leverage, B/M redundancia:** A B/M jelenlétében az earnings yield (E/P) és a leverage redundánssá válik — a B/M "absorbs" ezeket.

## Elméleti értelmezés

- **Kockázat-alapú:** A size és value prémiumok szisztematikus kockázatok kompenzációi — olyan kockázatokért, amelyeket a CAPM egyfaktoros béta nem ragad meg.
- **Kritika:** Lakonishok, Shleifer & Vishny (1994) later vitatják — szerintük a value prémium befektetői irracionális tévesítésen alapul, nem kockázaton.

## Jelentősége a wiki számára

- Ez az **FF3 modell közvetlen előfutára** — a Fama-French (1993) SMB és HML faktorok innen erednek
- Megcáfolja az CAPM egyetlen-faktor elégségességét
- Az FF1992 az egyik legtöbbet idézett pénzügyi papír — a faktorbefektetés empirikus alapköve
- Megjegyzés: scanned PDF, szöveges tartalom nem kinyerhető — source summary saját tudás alapján készült

## Kapcsolódó wiki oldalak

- [[entities/hml]] — B/M-alapú value faktor
- [[entities/smb]] — méretprémium
- [[entities/capm]] — amelyet ez a paper megcáfol
- [[source_summaries/fama-french-1993]] — a közvetlen folytatás
- [[open_questions/kke-factor-premiums]] — a B/M prémium KKE-ban is fennáll (Foye et al. 2016)
