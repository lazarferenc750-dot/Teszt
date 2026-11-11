---
title: "Claude tanfolyam"
subtitle: "Gyakorlati útmutató kezdőknek és haladóknak"
lang: hu-HU
toc-title: "Tartalomjegyzék"
date: "2026. november"
---

# Bevezetés

Ez a tanfolyam lépésről lépésre mutatja be, hogyan használhatod hatékonyan a Claude-ot, az Anthropic mesterséges intelligencia asszisztensét – a hétköznapi kérdésektől kezdve a dokumentumkészítésen át egészen a programozásig és az automatizálásig.

**Kinek szól?**

- Kezdőknek, akik most ismerkednek az AI-asszisztensekkel.
- Irodai és szakmai felhasználóknak, akik időt szeretnének spórolni a napi munkában.
- Fejlesztőknek, akik a Claude Code-ot vagy a Claude API-t szeretnék használni.

**Hogyan érdemes haladni?**

Minden modul végén találsz *gyakorló feladatokat*. A legtöbbet akkor tanulsz, ha a feladatokat ténylegesen ki is próbálod a Claude-dal. Nem kell egyszerre végigmenni az egészen – egy modul kb. 30–60 perc.

**A tanfolyam felépítése**

| Modul | Téma | Szint |
|---|---|---|
| 1 | Mi a Claude? | Kezdő |
| 2 | Az első lépések | Kezdő |
| 3 | A jó prompt alapjai | Kezdő |
| 4 | Haladó promptolási technikák | Középhaladó |
| 5 | Fájlok, dokumentumok, képek | Középhaladó |
| 6 | Projektek, artifactok és összekötők | Középhaladó |
| 7 | Claude a munkában – gyakorlati receptek | Középhaladó |
| 8 | Claude Code – programozás AI-val | Haladó |
| 9 | A Claude API alapjai | Haladó |
| 10 | Biztonság, adatvédelem, felelős használat | Mindenkinek |
| 11 | Záróprojekt | Mindenkinek |

# 1. modul – Mi a Claude?

## 1.1 Röviden

A Claude egy **nagy nyelvi modell** (Large Language Model, LLM), amelyet az Anthropic fejleszt. Szöveget, képet és dokumentumokat képes értelmezni, és ezek alapján válaszol, ír, elemez, összefoglal, fordít vagy programkódot készít.

A Claude nem keresőmotor és nem adatbázis: a válaszait a tanítás során megtanult mintázatok alapján *generálja*. Ezért nagyon jó gondolkodótárs és íróasszisztens – de a tényeket fontos ellenőrizni.

## 1.2 A modellcsaládok

Az Anthropic több méretben és képességszinten kínál modelleket. Általános ökölszabály:

- **Opus** – a legerősebb modellek, összetett gondolkodásra, nehéz programozási és elemzési feladatokra.
- **Sonnet** – kiegyensúlyozott: gyors és nagyon jó minőségű, a legtöbb napi feladatra ideális.
- **Haiku** – a leggyorsabb és legolcsóbb, egyszerű, nagy mennyiségű feladatokra (pl. osztályozás, rövid összefoglalók).

> **Tipp:** Ha bizonytalan vagy, kezdd az alapértelmezett modellel. Ha a válasz nem elég mély, válts erősebb modellre; ha csak gyorsaság kell, válts kisebbre.

## 1.3 Hol érhető el a Claude?

- **claude.ai** – webes felület böngészőben.
- **Asztali alkalmazás** (Windows, macOS) és **mobilalkalmazás** (iOS, Android).
- **Claude Code** – fejlesztőknek: terminálban, IDE-ben, asztali appban és a weben.
- **Claude API** – saját alkalmazásokba építhető.
- Integrációk más eszközökben (pl. Slack, böngészőbővítmény, irodai programok).

## 1.4 Mire jó és mire nem?

| Erősségek | Korlátok |
|---|---|
| Szövegírás, átfogalmazás, stílusváltás | Tévedhet, „hallucinálhat” tényeket |
| Összefoglalás hosszú dokumentumokból | Nem lát bele a gépedbe/fiókjaidba, hacsak nem kapcsolod össze |
| Ötletelés, tervezés, strukturálás | Friss eseményekről csak keresés segítségével tud |
| Programozás, hibakeresés | Számolásnál érdemes ellenőrizni vagy kódot futtatni |
| Fordítás, nyelvtanulás | Jogi, orvosi, pénzügyi kérdésben nem helyettesít szakembert |

## Gyakorló feladatok

1. Kérdezd meg a Claude-ot: „Mutasd be magad 5 mondatban, és mondd el, miben tudsz nekem segíteni egy irodai munkában!”
2. Kérj tőle egy olyan tényt, amit biztosan tudsz ellenőrizni (pl. a lakóhelyed lakosságszáma), és vesd össze egy hiteles forrással.

# 2. modul – Az első lépések

## 2.1 Regisztráció és felület

1. Nyisd meg a **claude.ai** oldalt, és regisztrálj e-mail címmel vagy Google-fiókkal.
2. A bal oldali sávban látod a korábbi **beszélgetéseidet** és a **projektjeidet**.
3. Középen az üzenetmező: ide írod a kérést, ide húzhatsz fájlokat, és itt választhatsz modellt.

## 2.2 Az első beszélgetés

Írj be egy egyszerű kérést, például:

```
Segíts megtervezni egy 3 napos budapesti kirándulást egy 4 fős családnak,
két 8–12 éves gyerekkel. Legyen benne napi program, étkezési ötlet és
becsült költség forintban.
```

Figyeld meg, hogy:

- a válasz **strukturált** (címsorok, listák),
- **folytathatod** a beszélgetést („Legyen az első nap esős időre tervezve!”),
- a Claude **emlékszik** a beszélgetés korábbi részeire.

## 2.3 Hasznos funkciók

- **Válasz újragenerálása** – ha nem tetszik, kérj új változatot.
- **Üzenet szerkesztése** – javítsd ki a saját kérdésed, és a beszélgetés onnan ágazik el.
- **Másolás** – egy kattintással kimásolhatod a választ.
- **Stílusok** – beállíthatod, hogy tömörebb, magyarázóbb vagy formálisabb legyen a válasz.
- **Webes keresés** – friss információkhoz bekapcsolható.
- **Memória és egyéni utasítások** – megadhatod, hogy mindig magyarul, tegeződve, röviden válaszoljon.

## Gyakorló feladatok

1. Állítsd be az egyéni utasításoknál: „Mindig magyarul válaszolj, tegezz, és a végén adj 1 mondatos összefoglalót.”
2. Kezdj egy beszélgetést, majd szerkeszd az első üzeneted, és figyeld meg, hogyan változik a válasz.

# 3. modul – A jó prompt alapjai

A **prompt** az az utasítás, amit a Claude-nak adsz. A válasz minősége nagyrészt a prompt minőségén múlik.

## 3.1 Az aranyszabály

> Úgy írj a Claude-nak, mintha egy okos, de a helyzetedet nem ismerő új kollégának adnál feladatot.

Egy új kolléga nem tudja, ki a célközönség, milyen hosszú legyen a szöveg, milyen hangnemben, és mire használod majd. Ezeket el kell mondani.

## 3.2 A jó prompt 5 eleme

1. **Szerep / kontextus** – Ki vagy, mi a helyzet?
2. **Feladat** – Pontosan mit kérsz?
3. **Célközönség** – Kinek szól az eredmény?
4. **Formátum** – Lista, táblázat, e-mail, max. hány szó?
5. **Példák és megkötések** – Mit kerüljön, mi legyen benne mindenképp?

## 3.3 Rossz és jó példa

**Gyenge prompt:**

```
Írj egy e-mailt a szabadságomról.
```

**Erős prompt:**

```
Egy uszoda műszakvezetője vagyok. Írj egy rövid, udvarias e-mailt a
csapatomnak arról, hogy december 22. és 27. között szabadságon leszek.
Helyettesítőm Kovács Anna lesz, sürgős ügyben őt keressék a belső
telefonszámon. Hangnem: barátságos, de hivatalos. Max. 120 szó.
Adj 2 változatot tárgysorral együtt.
```

## 3.4 Iteráció – a beszélgetés ereje

Ritkán sikerül elsőre tökéletesen. Finomíts:

- „Legyen rövidebb, max. 3 mondat.”
- „Kevesebb szakkifejezést használj.”
- „Tedd táblázatba.”
- „Mi hiányzik még ebből szerinted?”

## 3.5 Gyakori hibák

- **Túl általános kérés** – nincs cél, nincs közönség.
- **Több feladat egyben, rendezetlenül** – bontsd lépésekre.
- **Kontextus hiánya** – a Claude nem tudja, amit te tudsz.
- **Vakon elfogadott válasz** – mindig olvasd át és ellenőrizd.

## Gyakorló feladatok

1. Vegyél egy valódi munkahelyi feladatot, és írd meg először „gyenge”, majd „erős” promptként. Hasonlítsd össze a válaszokat.
2. Kérd meg a Claude-ot: „Javítsd ki a promptomat, hogy jobb eredményt kapjak:” – és másold be a saját promptod.

# 4. modul – Haladó promptolási technikák

## 4.1 Példák megadása (few-shot)

Ha konkrét formátumot vagy stílust szeretnél, mutass 1–3 példát:

```
Alakítsd át a vásárlói visszajelzéseket egy soros összefoglalóvá.

Példa:
Bemenet: "A víz hideg volt, de a személyzet kedves."
Kimenet: Negatív: vízhőmérséklet | Pozitív: személyzet

Most ezt:
Bemenet: "Tiszta öltöző, de sokat kellett várni a pénztárnál."
```

## 4.2 Lépésenkénti gondolkodás

Összetett feladatnál kérd, hogy előbb gondolja végig:

```
Mielőtt válaszolsz, gondold végig lépésről lépésre, milyen szempontok
számítanak, majd a végén adj egyértelmű javaslatot.
```

A modern Claude-modellek **kiterjesztett gondolkodás** (extended thinking) módban maguktól is képesek erre – bonyolult elemzésnél érdemes bekapcsolni.

## 4.3 Struktúra XML-címkékkel

Hosszabb anyagoknál segít, ha elválasztod a részeket:

```
<dokumentum>
...ide jön a szerződés szövege...
</dokumentum>

<feladat>
Gyűjtsd ki a határidőket és a fizetési feltételeket táblázatba.
</feladat>
```

## 4.4 Szerepjáték és nézőpontváltás

- „Viselkedj úgy, mint egy szigorú szerkesztő, és kritizáld a szövegemet.”
- „Te egy elégedetlen vendég vagy – milyen kérdéseket tennél fel?”
- „Érvelj a döntésem ellen, hogy lássam a gyenge pontjait.”

## 4.5 Kimenet formázása

Pontosan írd le, mit vársz:

- „Csak a táblázatot add vissza, magyarázat nélkül.”
- „JSON formátumban válaszolj, ezekkel a mezőkkel: nev, datum, osszeg.”
- „Markdown címsorokat használj, max. 3 szintet.”

## 4.6 Láncolás – nagy feladat kis lépésekben

Egy nagy feladatot (pl. egy 20 oldalas beszámoló) bonts lépésekre:

1. Vázlat (fejezetcímek) → jóváhagyod.
2. Fejezetenkénti kidolgozás.
3. Átolvasás, egységesítés, összefoglaló.

## Gyakorló feladatok

1. Készíts few-shot promptot, amely e-mailek tárgysorát három kategóriába sorolja: *sürgős*, *tájékoztató*, *reklám*.
2. Adj meg egy döntési helyzetet, és kérd, hogy a Claude „ördögügyvédként” érveljen ellene.

# 5. modul – Fájlok, dokumentumok, képek

## 5.1 Mit tölthetsz fel?

- **Dokumentumok:** PDF, Word (DOCX), szövegfájlok.
- **Táblázatok:** Excel (XLSX), CSV.
- **Képek:** fotók, képernyőképek, diagramok, kézírás.
- **Kód:** forrásfájlok bármilyen nyelven.

## 5.2 Tipikus feladatok

| Feladat | Példa prompt |
|---|---|
| Összefoglalás | „Foglald össze ezt a 40 oldalas jelentést 10 pontban.” |
| Adatkinyerés | „Gyűjtsd ki a számlákról a dátumot, összeget és szállítót táblázatba.” |
| Összehasonlítás | „Mi a különbség a két szerződésverzió között?” |
| Képelemzés | „Mi látható ezen a műszerfal-fotón? Olvasd le az értékeket.” |
| Táblázatelemzés | „Melyik hónapban volt a legmagasabb a gázfogyasztás, és miért lehet?” |

## 5.3 Fájlok létrehozása

A Claude nemcsak olvas, hanem **készíteni is tud** fájlokat: Excel-táblázatot képletekkel, Word-dokumentumot, PowerPoint-bemutatót vagy PDF-et. Egyszerűen kérd:

```
Készíts egy Excel-táblázatot a mellékelt adatokból: havonta egy sor,
oszlopok: hónap, fogyasztás (m³), költség (Ft). Legyen benne összesítő
sor és egy oszlopdiagram.
```

## 5.4 Tippek

- Nevezd meg, **melyik részre** figyeljen („a 3. fejezet táblázatára”).
- Nagyon hosszú anyagnál kérj **forrásmegjelölést** („add meg az oldalszámot is”).
- A számokat **ellenőrizd szúrópróbaszerűen** az eredeti dokumentumban.

## Gyakorló feladatok

1. Tölts fel egy PDF-et, és kérj belőle 5 pontos összefoglalót + 3 kérdést, amit egy megbeszélésen fel lehetne tenni.
2. Fotózz le egy kézzel írt listát, és kérd, hogy alakítsa táblázattá.

# 6. modul – Projektek, artifactok és összekötők

## 6.1 Projektek

A **projekt** egy tematikus munkaterület, ahol:

- feltöltheted az állandó háttéranyagokat (szabályzatok, sablonok, korábbi beszámolók),
- megadhatsz **projekt-utasításokat** („Minden beszámoló ebben a formátumban készüljön…”),
- a projekt összes beszélgetése ezekre épít.

**Példa:** egy „Havi beszámolók” projekt, amelyben benne van a beszámolósablon, és a projekt utasítása leírja a kötelező fejezeteket.

## 6.2 Artifactok

Az **artifact** egy külön ablakban megjelenő, önálló tartalom: dokumentum, weboldal, interaktív alkalmazás, diagram vagy kódrészlet. Előnyei:

- szerkeszthető és továbbfejleszthető a beszélgetésben,
- megosztható másokkal egy linkkel,
- interaktív eszközök is készíthetők (pl. kalkulátor, kvíz, műszakbeosztó tábla).

```
Készíts egy interaktív kalkulátort, amely a medence térfogatából és a
klórszintből kiszámolja a szükséges vegyszermennyiséget.
```

## 6.3 Összekötők (connectorok) és MCP

Az **összekötők** révén a Claude hozzáférhet más szolgáltatásokhoz – például Google Drive, Gmail, Google Naptár, Slack, Notion –, ha te engedélyezed. Így olyan kéréseket is teljesíthet, mint:

- „Keresd meg a Drive-on a legutóbbi gépészeti beszámolót, és foglald össze.”
- „Nézd meg a naptáramat, és javasolj egy szabad időpontot jövő hétre.”

A háttérben ezt a **Model Context Protocol (MCP)** teszi lehetővé: egy nyílt szabvány, amellyel bármilyen eszköz vagy adatforrás összekapcsolható az AI-val.

## 6.4 Skillek

A **skill** egy újrahasználható „recept”: utasítások, sablonok és szkriptek csomagja egy visszatérő feladathoz (pl. „havi beszámoló készítése”, „levél formázása céges stílusban”). Ha egy feladatot rendszeresen ugyanúgy végzel, érdemes skillt készíteni belőle – így minden alkalommal egységes lesz az eredmény.

## Gyakorló feladatok

1. Hozz létre egy projektet egy visszatérő feladatodhoz, tölts fel bele egy sablont, és írj hozzá projekt-utasítást.
2. Kérj egy egyszerű interaktív artifactot (pl. teendőlista vagy kvíz a tanfolyam anyagából).

# 7. modul – Claude a munkában: gyakorlati receptek

## 7.1 E-mailek és levelezés

```
Itt egy beérkezett panaszlevél. Írj rá empatikus, megoldásközpontú
választ, ami elismeri a hibát, felajánl egy kompenzációt (1 ingyenes
belépő), és max. 150 szó.
```

## 7.2 Beszámolók és jelentések

```
A mellékelt táblázat a havi energiafogyasztás adatait tartalmazza.
Készíts vezetői beszámolót: 1) összefoglaló 3 mondatban, 2) eltérések
az előző hónaphoz képest, 3) lehetséges okok, 4) javaslatok.
```

## 7.3 Beosztás és tervezés

```
Készíts műszakbeosztást decemberre 6 főre. Szabályok: napi 2 műszak
(6–14, 14–22), mindenkinek havonta max. 22 műszak, egymás után max.
5 nap, hétvégén legalább 2 fő műszakonként. A szabadságokat lásd lent.
```

> **Tipp:** Beosztásnál kérd, hogy a végén **ellenőrizze** a szabályok betartását, és listázza az esetleges ütközéseket.

## 7.4 Megbeszélések

- Napirend előkészítése a témák alapján.
- Jegyzetekből emlékeztető és teendőlista (ki, mit, meddig).
- Nehéz beszélgetés előtti felkészülés („Hogyan mondjam el a csapatnak…”).

## 7.5 Tanulás és fejlődés

- „Magyarázd el a kémiai vízkezelés alapjait egy 14 éves szintjén, majd egy szakember szintjén.”
- „Kérdezz ki 10 kérdéssel az elsősegélynyújtásról, és értékeld a válaszaimat.”
- „Készíts 4 hetes tanulási tervet Excel-függvényekhez, napi 20 percben.”

## 7.6 Kreatív munka

- Szlogenek, plakátszövegek, közösségi média posztok.
- Rendezvényötletek, nyereményjáték-szabályzat vázlata.
- Történetek, versek, köszöntők.

## Gyakorló feladatok

1. Válassz ki egy heti rendszerességű feladatot, és írj hozzá egy újrahasználható „sablonpromptot”.
2. Mérd le: mennyi idő volt a feladat Claude nélkül, és mennyi vele?

# 8. modul – Claude Code: programozás AI-val

## 8.1 Mi a Claude Code?

A **Claude Code** egy *ágensalapú* programozási eszköz: nemcsak kódot javasol, hanem önállóan olvassa a projekt fájljait, parancsokat futtat, teszteket indít, módosításokat végez és akár git-commitot is készít – mindezt a te jóváhagyásod mellett.

Elérhető:

- parancssorban (terminál),
- VS Code és JetBrains bővítményként,
- asztali alkalmazásban,
- a weben (claude.ai/code), felhőben futó munkamenetként.

## 8.2 Telepítés és indítás (terminál)

```bash
# telepítés (Node.js szükséges)
npm install -g @anthropic-ai/claude-code

# a projekt mappájában
cd sajat-projekt
claude
```

Az első indításkor be kell jelentkezni a Claude-fiókoddal.

## 8.3 Alapvető munkafolyamat

1. **Feltérképezés:** „Mutasd be, hogyan épül fel ez a projekt.”
2. **Tervezés:** „Tervezd meg, hogyan adnánk hozzá egy bejelentkezési oldalt. Még ne írj kódot.”
3. **Megvalósítás:** „Rendben, valósítsd meg a tervet.”
4. **Ellenőrzés:** „Futtasd a teszteket, és javítsd a hibákat.”
5. **Mentés:** „Készíts commitot érthető üzenettel.”

## 8.4 Hasznos parancsok és fogalmak

| Elem | Mire való |
|---|---|
| `CLAUDE.md` | Projektleíró fájl: szabályok, parancsok, konvenciók, amelyeket a Claude mindig figyelembe vesz |
| `/init` | Elkészíti a kezdeti `CLAUDE.md`-t |
| `/help` | Súgó |
| `/clear` | Új, tiszta kontextus |
| Plan mód | Először csak tervet készít, és jóváhagyásra vár |
| Engedélyek | Beállítható, mit csinálhat kérdés nélkül |
| Hookok | Automatikus műveletek bizonyos eseményekre (pl. formázás mentés után) |
| MCP-szerverek | Külső eszközök (adatbázis, GitHub, böngésző) bekötése |
| Subagentek | Részfeladatok párhuzamos, önálló végrehajtása |

## 8.5 Jó gyakorlatok

- **Kis lépésekben** dolgozz, és nézd át a változtatásokat (diff).
- Adj **ellenőrizhető célt**: „A tesztek legyenek zöldek.”
- Tartsd naprakészen a `CLAUDE.md`-t.
- Használj **git-et**, hogy bármikor visszaállhass.
- Érzékeny adatot (jelszó, API-kulcs) ne írj a promptba vagy a kódba.

## Gyakorló feladatok

1. Kérd meg a Claude Code-ot, hogy készítsen egy egyszerű HTML-oldalt (pl. időjárás-dashboard), majd fejlesszétek tovább három lépésben.
2. Futtasd az `/init` parancsot egy meglévő projektben, és nézd át a keletkezett `CLAUDE.md`-t.

# 9. modul – A Claude API alapjai

## 9.1 Mikor kell az API?

Ha a Claude-ot **saját alkalmazásba, weboldalba vagy automatizálásba** szeretnéd építeni – például egy ügyfélszolgálati chatbotba vagy egy dokumentumfeldolgozó rendszerbe.

## 9.2 Első lépések

1. Regisztrálj a **Claude Console**-on (console.anthropic.com), és hozz létre API-kulcsot.
2. Telepítsd a hivatalos SDK-t:

```bash
pip install anthropic
```

3. Állítsd be a kulcsot környezeti változóként:

```bash
export ANTHROPIC_API_KEY="ide-jon-a-kulcs"
```

## 9.3 Az első hívás (Python)

```python
import anthropic

client = anthropic.Anthropic()  # a kulcsot a környezeti változóból olvassa

message = client.messages.create(
    model="claude-sonnet-5-5",
    max_tokens=1024,
    system="Segítőkész asszisztens vagy, mindig magyarul válaszolsz.",
    messages=[
        {"role": "user", "content": "Adj 3 tippet a hatékony e-mailezéshez."}
    ],
)

print(message.content[0].text)
```

> A modellazonosítók idővel változnak – a mindenkori aktuális listát a hivatalos dokumentációban (docs.claude.com) találod.

## 9.4 Fontos fogalmak

- **Token** – a szöveg egysége (kb. szórészlet); a díjazás és a korlátok tokenben értendők.
- **System prompt** – az állandó viselkedési utasítás.
- **Kontextusablak** – mennyi szöveget „lát” egyszerre a modell.
- **Streaming** – a válasz folyamatos, darabonkénti érkezése.
- **Tool use** – a modell saját függvényeidet hívhatja meg (pl. adatbázis-lekérdezés).
- **Prompt caching** – az ismétlődő hosszú kontextus gyorsítótárazása, ami csökkenti a költséget és a késleltetést.
- **Batch API** – nagy mennyiségű kérés olcsóbb, nem valós idejű feldolgozása.

## Gyakorló feladatok

1. Írj egy szkriptet, amely egy szövegfájl tartalmát beolvassa, és 5 pontos összefoglalót kér róla.
2. Módosítsd úgy, hogy az eredményt JSON-ként adja vissza (`cim`, `pontok` mezőkkel).

# 10. modul – Biztonság, adatvédelem, felelős használat

## 10.1 Adatvédelem

- **Ne ossz meg** feleslegesen személyes adatot (személyi szám, egészségügyi adat, jelszó, bankkártya).
- Céges anyagnál tartsd be a munkahelyi **AI-használati szabályzatot**.
- Ellenőrizd a fiókod **adatvédelmi beállításait** (pl. hogy a beszélgetések felhasználhatók-e a modellek fejlesztésére).
- Csapat- és vállalati előfizetéseknél külön adminisztrációs és adatkezelési szabályok érvényesek.

## 10.2 Ellenőrzés és felelősség

- A Claude **tévedhet**. Fontos számot, dátumot, jogszabályt, idézetet mindig ellenőrizz.
- Az elkészült anyagért **te felelsz** – olvasd át, mielőtt elküldöd.
- Kérj **forrást** és **bizonytalansági jelzést**: „Jelöld, miben nem vagy biztos.”

## 10.3 Prompt injection

Ha a Claude külső tartalmat olvas (weboldal, e-mail, dokumentum), abban lehetnek „rejtett utasítások”, amelyek félre akarják vezetni. Ezért:

- olyan eszközöknél, amelyek műveletet végeznek (e-mail küldés, fájltörlés), **mindig nézd át**, mit hagysz jóvá,
- ne adj szélesebb jogosultságot, mint amire a feladathoz szükség van.

## 10.4 Etikus használat

- Jelezd, ha egy anyag jelentős részben AI-val készült, ahol ez elvárás.
- Ne használd mások megtévesztésére, hamis dokumentumok készítésére.
- A szerzői jogokat és mások személyiségi jogait tartsd tiszteletben.

## Gyakorló feladatok

1. Nézd át a fiókod adatvédelmi beállításait.
2. Írj egy rövid, 5 pontos „AI-használati szabályt” a saját csapatodnak.

# 11. modul – Záróprojekt

Válassz egyet az alábbiak közül, és valósítsd meg a Claude segítségével:

**A) Irodai automatizálás**
Hozz létre egy projektet egy visszatérő beszámolódhoz (sablon + utasítás), és készítsd el vele a következő havi beszámolót elejétől a végéig.

**B) Interaktív eszköz**
Készíts egy artifactot, ami a munkádat segíti (kalkulátor, ellenőrzőlista, beosztástábla), és oszd meg egy kollégával.

**C) Fejlesztői projekt**
A Claude Code segítségével készíts egy kis webalkalmazást, `CLAUDE.md`-vel, tesztekkel és legalább 3 commit-tal.

**Értékelési szempontok:**

- Világos volt-e a cél és a prompt?
- Hány iterációból jutottál el a kész eredményig?
- Mit ellenőriztél, és találtál-e hibát?
- Mennyi időt spóroltál?

# Függelék

## A. Prompt-sablonok gyűjteménye

**Általános feladat**

```
Szerep: [ki vagy / milyen helyzetben]
Feladat: [pontosan mit kérsz]
Célközönség: [kinek szól]
Formátum: [lista / táblázat / e-mail, hossz]
Megkötések: [mit kerüljön, mi legyen benne]
```

**Összefoglalás**

```
Foglald össze az alábbi szöveget [N] pontban [célközönség] számára.
A végén emeld ki a 3 legfontosabb teendőt.
<szoveg>...</szoveg>
```

**Átírás**

```
Írd át az alábbi szöveget [hangnem] hangnemben, [hossz] terjedelemben,
a lényeges információk megtartásával.
```

**Kritika**

```
Értékeld a szövegemet egy tapasztalt szerkesztő szemével: 3 erősség,
3 gyengeség, és konkrét javítási javaslatok.
```

## B. Szószedet

| Fogalom | Jelentés |
|---|---|
| LLM | Nagy nyelvi modell, a Claude alapja |
| Prompt | Az utasítás, amit a modellnek adsz |
| Token | A szöveg feldolgozási egysége |
| Kontextusablak | Az egyszerre feldolgozható szövegmennyiség |
| Hallucináció | Magabiztosan közölt, de téves információ |
| Artifact | Önálló, külön ablakban megjelenő tartalom |
| Projekt | Tematikus munkaterület saját anyagokkal és utasításokkal |
| MCP | Nyílt szabvány külső eszközök és adatok bekötésére |
| Skill | Újrahasználható utasítás- és sablon-csomag |
| Ágens (agent) | Önállóan, több lépésben dolgozó AI, eszközöket használva |
| System prompt | Állandó viselkedési utasítás (API-ban) |

## C. Hasznos források

- Claude súgóközpont: support.claude.com
- Fejlesztői dokumentáció: docs.claude.com
- Claude Code dokumentáció: code.claude.com
- Anthropic Academy – ingyenes angol nyelvű kurzusok: anthropic.com/learn
- Anthropic nyilvános kurzusanyagai: github.com/anthropics/courses

---

*Jó tanulást és eredményes munkát a Claude-dal!*
