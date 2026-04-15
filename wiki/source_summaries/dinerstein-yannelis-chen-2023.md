---
type: source_summary
tags: [macro-factor, credit, liquidity, consumer-finance, usa]
confidence: high
last_reviewed: 2026-04-15
related: [[concepts/factor-cyclicality]], [[open_questions/kke-factor-premiums]]
---

# Dinerstein, Yannelis & Chen (2023) — Debt Moratoria: Evidence from Student Loan Forbearance

**Forrás:** NBER Working Paper No. 31247, 2023. május  
**Szerzők:** Michael Dinerstein (U Chicago), Constantine Yannelis (Chicago Booth), Ching-Tse Chen (U Chicago)  
**Fájl:** `raw/raw/w31247.pdf`

## Fő állítás

A 2020-as diákhitel-moratórium (payment pause) vizsgálata alapján: a likviditásnövekedés **nem az adósságcsökkentésre, hanem új hitelkereslet generálására** fordítódott. A kormányzati adósságmoratórium stimulus-hatása nagyobb volt, mint a bejelentett adósság-elengedés (balance discharge) ígérete.

## Módszertan

- **Természetes kísérlet:** A Direct Loan (DL) vs. Federal Family Education Loan (FFEL) program adminisztratív különbsége: 2020-ban csak a DL kölcsönökre vonatkozott a fizetési szünet, az FFEL-ekre nem (jogi tulajdon kérdése).
- **Különbség-a-különbségben (DiD):** DL vs FFEL hitelfelvevők összehasonlítása.
- **Adat:** TransUnion adminisztratív hitelpanel — USA 10%-os mintája hitelhistóriával rendelkező személyekből.
- **Horizont:** 2019–2022.

## Főbb eredmények

1. **Likviditás-hitel komplementaritás:** A moratórium nem csökkentette a háztartások eladósodottságát — épp ellenkezőleg, +$1,200 (3%) növekedés nem-diákhitel állományban. A hitelfelvevők jelzáloghitelre, autóhitelre, hitelkártyára fordítottak a felszabaduló likviditást.
2. **Stimulus koncentrációja:** A hatás csak a korábban nem volt hátralékos hitelfelvevőknél érvényesült — akiknek hitelkínálata nem változott, csak hitelkeresletük nőtt a likviditás hatására.
3. **Adósság-elengedés vs. moratórium:** Az adósság-elengedés bejelentése (balance forgiveness) szignifikánsan kisebb fogyasztási hatást váltott ki, mint az azonnal felszabaduló likviditás.

## Relevanciája a faktor trading wiki számára

**Közvetlen relevancia: alacsony.** A tanulmány US fogyasztói pénzügyekre fókuszál, nem részvényfaktor-prémiumokra.

**Közvetett kapcsolatok:**
- **Makro-rezsim:** Kormányzati beavatkozás (debt forbearance) → hitelciklus → fogyasztás → részvénypiaci makro faktor kontextus
- **Likviditás-faktor:** A likviditás-hitelkereslet komplementaritás elvként átvihető: ha szektoriális likviditásinjekció nő, az érintett szektorra vetítve *felfelé torzíthatja a momentum/quality faktorokat* (nem eladósodott, jobb minőségű cégek profitálnak a keresletnövekedésből)
- **KKE analógia:** A KKE piacokon az EU-s transzfer-programok és nemzeti moratóriumok (pl. 2020 magyar hitelmoratórium) hasonló mechanizmust indíthatnak el — de ez még teszteletlen hipotézis

## Limitációk

- Kizárólag US-specifikus intézményi keretben érvényes (DL/FFEL különbség)
- 2019–2022 időszak, COVID-specifikus rezsim
- A mechanizmus (likviditás → hitelkereslet) nem biztos, hogy más piacokra általánosítható

## Hivatkozott módszertani eszközök

- Különbség-a-különbségben (DiD) regresszió
- Lokális projekciók (Jordà 2005 stílusban)
- Administatív panel adat + kétirányú fixed effects
