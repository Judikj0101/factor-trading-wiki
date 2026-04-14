# Factor Trading Wiki — Schema

Ez a fájl írja le hogyan működik a wiki. Minden LLM agent (Claude Code, Codex, bármilyen agent) ezt olvassa el először mielőtt bármit csinál a vault-ban.

## A rendszer célja

Kuratált, szintetizált, élő faktor trading tudásbázis. Nem dokumentumtár — hanem feldolgozott, kereszthivatkozott, ellentmondás-tudatos enciklopédia. A wiki compound-ol: minden új forrás gazdagítja a meglévő tudást, nem csak mellé kerül.

## Architektúra

Három réteg:

### 1. Raw sources (`raw/`)
- Immutable. Az LLM **soha nem módosítja** ezeket.
- Almappák: `papers/`, `datasets/`, `standards/`, `code/`
- Ide kerülnek: academic papers, GDELT dokumentáció, CAMEO kódtáblák, piaci adatok, backteszt eredmények, kódrészletek.

### 2. Wiki (`wiki/`)
- Az LLM által karbantartott réteg. Markdown + wikilinks.
- Az LLM **szabadon létrehozhat, módosíthat és törölhet** oldalakat ebben a mappában.
- Hat oldaltípus (lásd lent).
- Speciális fájlok: `index.md`, `log.md`, `contradictions.md`

### 3. Schema (ez a fájl)
- Az LLM és a felhasználó **közösen** fejleszti.
- Változtatás előtt mindig egyeztetés a felhasználóval.

## Oldaltípusok

Minden wiki oldal tetején YAML frontmatter:

```yaml
---
type: entity | concept | methodology | source_summary | comparison | open_question
tags: [relevant-tag-1, relevant-tag-2]
confidence: high | medium | low | contested
last_reviewed: YYYY-MM-DD
related: [[Kapcsolódó oldal 1]], [[Kapcsolódó oldal 2]]
---
```

### Entity pages (`wiki/entities/`)
Konkrét, megnevezhető dolgok: módszerek, mutatók, adatforrások, modellek.
- Példák: Kelly-kritérium, GDELT Tone, Fama-French SMB, VaR, Sharpe-ráta, CAMEO kódrendszer
- Tartalom: definíció, hogyan kapcsolódik a factor trading rendszerhez, limitációk, nyitott kérdések
- Fájlnév: `kelly-kriterium.md`, `gdelt-tone.md`, `fama-french-smb.md`

### Concept pages (`wiki/concepts/`)
Absztrakt fogalmak amik entitásokon átívelnek.
- Példák: Faktor validáció, Factor zoo probléma, Beárazódási sebesség, Rezsimváltás, Strukturális törés, Overfitting vs valódi szignifikancia
- Tartalom: mi ez, miért fontos, hogyan kapcsolódik más fogalmakhoz, milyen entitásokat érint
- Fájlnév: `faktor-validacio.md`, `factor-zoo.md`, `rezsimdetekcio.md`

### Methodology pages (`wiki/methodology/`)
Standard eljárások lépésről lépésre.
- Példák: Event study végrehajtás, Granger-teszt, Backteszt felépítése, Pozícióméretezés Kelly-vel, Portfólió optimalizálás Markowitz-cal
- Tartalom: mikor használjuk, előfeltételek, lépések, gyakori hibák, döntési pontok
- Fájlnév: `event-study.md`, `granger-teszt.md`, `kelly-poziciomeretezs.md`

### Source summaries (`wiki/source_summaries/`)
Minden feldolgozott forrás kivonata.
- Tartalom: fő állítások, releváns eredmények, limitációk, hogyan kapcsolódik a rendszerhez
- Fájlnév: a forrás rövid neve, pl. `fama-french-1993.md`, `gdelt-technical-doc.md`

### Comparisons (`wiki/comparisons/`)
Két vagy több dolog összevetése.
- Példák: GDELT Tone vs Goldstein skála, KKE vs USA piac GDELT hatás, ETF vs egyedi részvény event study-ban
- Tartalom: miben hasonlítanak, miben különböznek, mikor melyiket használd
- Fájlnév: `tone-vs-goldstein.md`, `kke-vs-usa-gdelt.md`

### Open questions (`wiki/open_questions/`)
Amit nem tudunk, amit tesztelni kell, ahol gap van.
- Tartalom: a kérdés precíz megfogalmazása, miért fontos, milyen forrásra lenne szükség a megválaszolásához, milyen wiki oldalakat érint
- Fájlnév: `gdelt-kke-szignifikancia.md`, `rezsimdetekcio-automatizalas.md`

## Confidence szintek

- **high** — több független forrás megerősíti, konszenzus van, robusztus eredmények
- **medium** — egy-két forrás támogatja, de nincs széleskörű validáció
- **low** — spekulatív, egy forrás, vagy a felhasználó saját hipotézise validáció nélkül
- **contested** — források ellentmondanak egymásnak. Ilyenkor a `contradictions.md` is frissül.

Confidence változhat — ha új forrás megerősít vagy megcáfol egy állítást, frissíteni kell.

## Műveletek (Operations)

### Ingest — új forrás feldolgozása

1. A felhasználó elhelyezi a forrást a `raw/` megfelelő almappájában.
2. Az LLM elolvassa a forrást.
3. Megbeszéli a felhasználóval a fő tanulságokat (ha a felhasználó elérhető).
4. Létrehoz egy source summary oldalt a `wiki/source_summaries/`-ban.
5. Végigmegy a wiki-n és frissíti az érintett entity, concept, methodology oldalakat:
   - Új információ hozzáadása
   - Confidence frissítése ha szükséges
   - Ellentmondás jelzése ha az új forrás mond ellent meglévő tartalomnak → `contradictions.md` frissül
   - Hiányzó oldalak létrehozása ha az új forrás olyan entitásra vagy fogalomra hivatkozik ami még nem létezik
6. `index.md` frissítése az új/módosított oldalakkal.
7. `log.md`-be bejegyzés:
   ```
   ## [YYYY-MM-DD] ingest | Forrás neve
   - Source summary: [[source_summaries/forras-neve]]
   - Frissített oldalak: [[entities/xyz]], [[concepts/abc]]
   - Új oldalak: [[entities/uj-dolog]]
   - Ellentmondások: igen/nem
   ```

### Query — kérdés megválaszolása

1. Az LLM először az `index.md`-t olvassa el a releváns oldalak megtalálásához.
2. Beolvassa a releváns wiki oldalakat.
3. Szintetizált választ ad.
4. Ha a válasz értékes szintézis (comparison, új összefüggés, kutatási irány):
   - Felajánlja hogy wiki oldalként menti el
   - A felhasználó dönt
   - Ha igen → megfelelő oldaltípusba kerül, index és log frissül

### Lint — karbantartás

Futtatás: session elején vagy a felhasználó kérésére.

Ellenőrzési pontok:
- **Árva oldalak** — nincs bejövő wikilink (semmi nem hivatkozik rá)
- **Halott linkek** — wikilink mutat rá de az oldal nem létezik
- **Elavult oldalak** — `last_reviewed` > 60 nap
- **Hiányzó cross-reference-ek** — két oldal ugyanarról a témáról beszél de nem linkelnek egymásra
- **Confidence review** — `contested` oldalak átnézése: megoldódott-e az ellentmondás?
- **Open questions review** — megválaszolódott-e valamelyik kérdés az új források alapján?

Eredmény: lista a problémákkal. A felhasználó dönt a javításról.

## Konvenciók

### Fájlnevek
- Kisbetűs, kötőjeles: `kelly-kriterium.md`, nem `Kelly Kritérium.md`
- Angol terminológia a fájlnévben (a tartalom magyar): `event-study.md`, nem `esemeny-tanulmany.md`
- Rövid, egyértelmű

### Wikilinks
- Obsidian-stílusú: `[[entities/kelly-kriterium]]`
- Relatív a vault gyökeréhez képest
- Alias használata ha szükséges: `[[entities/kelly-kriterium|Kelly-kritérium]]`

### Tartalom nyelve
- Magyar, hacsak a felhasználó nem kér mást
- Angol szakkifejezések megtartása ahol az a standard (alpha, beta, Sharpe ratio, drawdown)
- Képletek LaTeX formátumban ahol releváns

### Tags
A frontmatter `tags` mezőjében használt címkék:
- Témakörök: `factor-model`, `gdelt`, `event-study`, `portfolio`, `risk-management`, `backtesting`, `sentiment`, `statistics`
- Piacok: `kke`, `usa`, `global`
- Módszer: `regression`, `time-series`, `cross-section`, `machine-learning`

## Tiltott műveletek

- Az LLM **soha nem módosítja** a `raw/` mappa tartalmát.
- Az LLM **soha nem törli** a `log.md` korábbi bejegyzéseit (append-only).
- Az LLM **soha nem változtatja** a confidence szintet a felhasználó tudta nélkül `contested` oldalak esetén.
- Az LLM **soha nem ír felül** ellentmondásos tartalom esetén — jelöli és megbeszéli a felhasználóval.

## Bootstrapping

Ha a vault üres (első használat), az LLM:
1. Elolvassa ezt a schema fájlt.
2. Feltérképezi a `raw/` tartalmát.
3. Javaslatot tesz az első ingest sorrendre.
4. Létrehozza az `index.md`, `log.md`, `contradictions.md` alapjait.
5. Megkezdni az első forrás feldolgozását a felhasználóval együtt.
