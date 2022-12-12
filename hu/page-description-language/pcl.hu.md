{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PCL",
  "description":"További információ a PCL fájlformátumról és az API-król, amelyek PCL fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "PCL",
  "menu" : {
    "docs" : {
      "parent" : "page-description-language"
}
},
  "lastmod" : "2019-09-10"
}

## Mi az a PCL fájl? ##

A PCL a Printer Command Language rövidítése, amely a Hewlett Packard (HP) által bevezetett oldalleíró nyelv. A HP azért hozta létre a PCL-t, hogy hatékony módot biztosítson a nyomtató funkcióinak vezérlésére számos különböző nyomtatóeszközön. A formátumot eredetileg a HP mátrix- és tintasugaras nyomtatóihoz fejlesztették ki, de az idő múlásával különféle hő-, mátrix- és oldalnyomtatók része lett. A formátum több különböző revízión esett át, aminek eredményeként különböző verziók születtek, ahol mindegyik verziót továbbfejlesztették, hogy megfeleljenek a nyomtatóvezérlési funkciók időigényének. Ma a PCL a legelterjedtebb nyomtatónyelv a legújabb nyomtatók piacán.

## PCL verziók ##

A PCL verziók funkcionalitásban különböznek (pl. betűtípus-támogatás: bittérképes betűtípusok, méretezhető betűtípusok (Intellifonts, TrueType betűtípusok), rasztergrafikus tömörítési módszerek, HP-GL/2 grafikai támogatás).

**PCL 1:** 1980 körül – A Print and Space funkció az egyszerű, kényelmes, egyfelhasználós munkaállomási kimenethez biztosított funkciók alapkészlete.

**PCL 2:** 1980 körül – Az EDP (elektronikus adatfeldolgozás)/tranzakció funkció a PCL 1 szuperkészlete. A funkciókat általános célú, többfelhasználós rendszerű nyomtatáshoz adták hozzá.

**PCL 3**: 1984 – Az Office Word Processing funkció a PCL 2 szuperkészlete. Funkciókkal egészült ki a kiváló minőségű irodai dokumentumkészítés és 300 dpi-ig növelt dpi. Korlátozott számú bittérképes betűtípus és grafika használatát tette lehetővé, és támogatta a HP-GL-t. A PCL 3-at más nyomtatógyártók széles körben utánozták, és ezek a cégek „LaserJet Plus Emulation” néven hivatkoztak rá.
(Nyomtatók: HP DeskJet család, HP LaserJet sorozatú nyomtató, HP LaserJet Plus sorozat nyomtató)

**PCL3+:** A DeskJet és a DesignJet nyomtatócsalád használja.

**PCL3c:** A DeskJet és a DesignJet nyomtatócsalád használja.

**PCL3e**: DeskJet és DesignJet nyomtatócsalád használja. Most a PhotoSmartban is használják.

**PCL3GUI**: RTL-t használ, és a DeskJet és a DesignJet nyomtatócsalád használja.

**PCLSLEEK**: RTL-t használ, és a DeskJet és a DesignJet nyomtatócsalád használja.

**PCL 4**: 1985 – Az oldalformázási funkció a PCL 3 szuperkészlete. Támogatott makrók, nagyobb bittérképes betűtípusok és grafikák. (Nyomtatók: HP LaserJet II, HP LaserJet IIP (PCL 4.5))

**PCL 5:** 1990 – Az Office Publishing funkció a PCL 4 szuperkészlete. Az új közzétételi lehetőségek közé tartozik a betűkészlet-méretezés és a HP-GL/2 (vektor) grafika. (Nyomtatók: HP LaserJet III)

**PCL 5e:** 1994 – Ez egy jelentős átdolgozás, amely olyan új funkciókat tartalmaz, mint az Adaptive Compression System, a 2 byte-os karakterkódolás, a vektoros betűtípusok támogatása és a kétirányú konfigurációs parancsok. Tartalmazza a logikai műveleteket (megfelel a GDI ROP-oknak), hogy javítsa a Windows támogatását a vágógörbék előtt. (Nyomtatók: HP LaserJet 4)

**PCL 5j:** Új funkciók, mint például a 2 bájtos karakterek támogatása a japán rezidens méretezhető betűtípusokhoz, függőleges írás, japán papírméretek és betűtípusok. (Nyomtatók: HP LaserJet 4PJ)

**PCL 5c:** 1995 – Színtámogatás és logikai műveletek kerültek a PCL5-be. A PCL5c megelőzi a PCL5e-t. Egyes modellek a vágógörbéket is támogatják. (Nyomtatók: HP Color LaserJet, HP PaintJet 300 XL (első nyomtató PCL5c-vel), HP DeskJet 1200C/1600C (ezeket a típusszámokat újra használták, és az újabb modellek nem PCL 5c)

**PCL 5ce:** Támogatja az Agfa Microtype méretezhető betűtípusokat. (Nyomtatók: HP 2500c Pro nyomtató)

**PCL 6 / XL:** 1996 - A PCL 6 vagy a PCL XL egy 1995-ben bevezetett új formátum, amely nem kompatibilis a PCL korábbi verzióival. (Nyomtatók: HP LaserJet 5, 5M és 5N)

## PCL 6 áttekintése ##

A HP 1996-ban mutatta be a PCL 6-ot, amely a PCL nyelv és a kapcsolódó technológiák következő evolúciója volt. A következő összetevőket tartalmazza:

**PCL 6 Enhanced:** optimalizált verziót biztosít grafikus felhasználói felületekről (GUI), például MS Windows és OS/2 történő nyomtatáshoz

**PCL 6 szabvány:** teljes visszamenőleges kompatibilitást biztosít a korábbi HP LaserJet nyomtatókkal

**PCL Font Synthesis:** méretezhető betűtípusokat, betűkészletkezelést, valamint űrlapok és betűtípusok tárolását biztosítja.

A PCL XL bővített verziója közelebb áll a GDI-hez, amelyet sok alkalmazás használ. Gondoskodik arról, hogy kevesebb fordításra kerüljön sor, ami megnövelt WYSIWYG-képességeket és jobb teljesítményt eredményez az Enhanced illesztőprogram által megvalósított kilépéseket támogató alkalmazásokkal. Előfordulhat, hogy az Enhanced (PCL XL) illesztőprogram kimenete nem egyezik meg a szabványos illesztőprogram kimenetével. Ha a kimenet nem a vártnak felel meg, válassza helyette a Standard (PCL5e) illesztőprogramot.

A PCL 6 Enhanced parancsokat úgy tervezték, hogy optimálisan megfeleljenek a grafikus felhasználói felület alapú alkalmazások grafikus nyomtatási követelményeinek. A legtöbb esetben minden grafikus felhasználói felület által végrehajtani kívánt grafikus nyomtatási parancshoz tartozik egy megfelelő PCL 6 Enhanced parancs. Ez csökkenti a grafikus oldal leírásához szükséges parancsok számát. A PCL 6 Enhanced minden egyes parancsa minimális adatátvitelt igényel a gazdaszámítógépről a nyomtatóra. Ez csökkenti az oldal leírásához szükséges adatok mennyiségét.

A Windows nyomtatórendszer a legtöbb HP LaserJet nyomtatóhoz két különálló illesztőprogramot biztosít: Standard és Enhanced. A Standard illesztőprogram visszamenőleges kompatibilitást biztosít a PCL 6 Standard (PCL5e) parancsok használatával egyszerű szöveges vagy vegyes szöveges és grafikus oldalak nyomtatásához. Az Enhanced illesztőprogram a PCL 6 Enhanced parancsait használja, amelyeket összetett grafikus oldalak nyomtatására optimalizáltak.

## PCL 6 osztályú változatok ##

#### 1.1 osztály ####

**Rajzeszközök:** Támogatják a vonalak, ívek/ellipszisek/akkordok, (lekerekített) téglalapok, sokszögek, Bezier-görbék, vágott görbék, raszterképek, pásztázási vonalak, raszteres műveletek rajzolását.
**Színkezelés:** 1/4/8 bites paletták, RGB/szürke színtér támogatása. Támogatja az egyéni féltónus mintákat (maximum 256 minta).
**Tömörítés:** Támogatja az RLE-t.
**Mértékegységek:** hüvelyk, milliméter, tizedmilliméter.
**Papírkezelés:** Egyedi vagy előre meghatározott papírtípusok támogatása, beleértve a szokásos Letter, Legal, A4 stb. papírokat. Választhat papírt a kézi adagolásból, tálcákból és kazettákból. A papír vízszintesen vagy függőlegesen kétoldalasan nyomtatható. A papír tájolható álló, fekvő vagy az előbbi kettő 180 fokos elforgatásával.
**Betűtípus:** Támogatja a bittérképes vagy TrueType betűtípusokat, 8 vagy 16 bites kódpontokat. A karakterkészlet kiválasztása a PCL 5-től eltérő szimbólumkészlet-kódot használ. Bittérképes betűkészlet használata esetén sok skálázási parancs nem érhető el. Ha TrueType betűtípust használ, a változó hosszúságú leírók és a folytatásos blokkok nem támogatottak. A körvonal betűtípusa forgatható, méretezhető vagy nyírható.

#### 2.0 osztály ####

**Tömörítés:** Egy szabadalmaztatott, JetReady nevű JPEG-tömörítés került hozzáadásra.
**Papírkezelés:** A hordozók különböző kimeneti tálcákra irányíthatók át (legfeljebb 256). Hozzáadott A6 és japán B6 előre beállított médiaméretek. Hozzáadott harmadik kazetta előre beállított, 248 külső tálca médiaforrás.
**Betűtípus:** A szöveg függőlegesen írható.

#### 2.1 osztály ####

**Színkezelés:** Színillesztési funkció hozzáadva.
**Tömörítés:** Delta sor hozzáadva.
**Papírkezelés:** A tájolás, a hordozóméret nem kötelező az új oldal deklarálásakor. B5, JIS 8K, JIS 16K, JIS Exec papírtípusok hozzáadva.

#### 3.0 osztály ####

**Színkezelés:** Lehetővé teszi a különböző féltónus-beállítások használatát vektor- vagy rasztergrafikákhoz, szövegekhez. Támogatja az adaptív féltónuszást.
**Protokoll:** Támogatja a PCL áthárítást, lehetővé téve a PCL 5 szolgáltatások használatát a PCL 6 adatfolyamok számára. Ennek a funkciónak a használatakor azonban egyes PCL 6 állapotok nem maradnak meg.
**Betűtípus:** Támogatja a PCL betűtípusokat.
**Néző/átalakító:** A PCLReader (ingyenes szoftver) bármilyen szintű PCL 6 (beleértve a JetReadyt is) megtekintésére, konvertálására vagy nyomtatására képes bármilyen nyomtatóra.

## Hivatkozások ##

* [PCL – a Wikipedia által](https://en.wikipedia.org/wiki/Printer_Command_Language)

