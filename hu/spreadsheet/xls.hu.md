{
  "date" : "2019-12-16",
  "keywords" :[ "XLS", "file", "extension", "file format", "Excel", "Spreadsheet" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"A fájlformátum útmutatója, hogy megtudja, mi az XLS-fájl és API-k, amelyek létrehozhatják és megnyithatják azokat.",
  "title" :"Mi az XLS fájlformátum? Tanuljon a fájlformátum-szakértőktől!",
  "linktitle" : "XLS",
  "menu" : {
    "docs" : {
      "parent" : "spreadsheet"
}
},
  "lastmod" : "2019-12-16"
}

## Mi az XLS fájl?

Az XLS kiterjesztésű fájlok Excel bináris fájlformátumot képviselnek. Ilyen fájlokat létrehozhat a Microsoft Excel, valamint más hasonló táblázatkezelő programok, például az OpenOffice Calc vagy az Apple Numbers. Az Excel által mentett fájl munkafüzetként ismert, ahol minden munkafüzet egy vagy több munkalappal rendelkezhet. Az adatok tárolása és megjelenítése a felhasználók számára táblázat formátumban, munkalapon történik, és kiterjedhetnek számértékekre, szöveges adatokra, képletekre, külső adatkapcsolatokra, képekre és diagramokra. Az olyan alkalmazások, mint a Microsoft Excel, lehetővé teszik a munkafüzet adatainak több különböző formátumba történő exportálását, beleértve a [PDF](/hu/pdf/), [CSV](/hu/spreadsheet/csv/), [XLSX](/hu/spreadsheet/xlsx/), [TXT](/hu/) szövegszerkesztő/txt/), [HTML](/hu/web/html/), [XPS](/hu/page-description-language/xps/) és még sok más. Az XLS fájlformátumot egy nyitottabb és strukturáltabb formátum, az XLSX váltotta fel a Microsoft Excel 2007 kiadásával. A legújabb verziók továbbra is támogatják az XLS fájlok létrehozását és olvasását, bár most az XLSX az első számú választás.

## Rövid története

Az XLS-t a Microsoft a Microsoft Excellel való használatra készítette, és Binary Interchange File Format (BIFF) néven is ismert. Ezt a fájltípust először az Excel for Windows részévé tették 1987-ben. Az XLS fájlformátum specifikációit először 2008 júniusában hozták nyilvánosságra 1. változat néven. Ezt követően a specifikációkat folyamatosan frissítették, és elérhetővé vált a legújabb verzió. 2018 augusztusi állapotú, és 8.0-s verzióként van megjelölve. Az XLS fájlformátum különböző verzióinak rövid története a következő:

* 7.0-s verzió (kiadva az Office 95-tel): Az Excel ezen verziója volt a legrobusztusabb és gyorsabb az összes verzió közül, és a belső adatfolyam-átírásokat 32 bitesre frissítették.
* 8-as verzió (kiadva az Office 97-tel): A VBA-t szabványos nyelvként vezették be, és ebbe a verzióba először eltávolították a természetes nyelvű címkéket. Először bevezetett egy irodai segédeszközt is.
* 9-es verzió (kiadva az Office 2000-ben): A 9-es verzióban csak kisebb változtatások történtek, ahol a gemkapocs irodai asszisztens egyszerre több objektumot tudott tárolni, ami korábban nem volt lehetséges.
* 10-es verzió (Office XP-vel megjelent): Ez a verzió nem tartalmazott észrevehető fejlesztést.
* 11-es verzió (az Office 2003-ban megjelent): A 11-es verzió főbb frissítése, az Excel 2003 új táblák bevezetése volt.

## XLS fájlformátum specifikációi ##

Az adatok XLS-fájlban vannak elrendezve bináris adatfolyamként összetett fájl formájában, az [MS-CFB]-ben leírtak szerint. Az adatok tárolása az összetett fájlban tárolók, adatfolyamok és alfolyamok használatával történik, amelyek a munkafüzet tartalmáról és szerkezetéről tartalmaznak információkat, beleértve a munkafüzetadatokat, például a munkalap-definíciókat. Minden adatfolyam vagy alfolyam bináris rekordok sorozatát tartalmazza. Minden bináris rekord nulla vagy több strukturált mezőt tartalmaz, amelyek a munkafüzet adatait tartalmazzák. Ez a rész rövid áttekintést ad az XLS fájlszerkezetről, de a részletes fájlformátum-specifikációkért olvassa el az [XLS fájlformázási specifikációkat] (https://msdn.microsoft.com/en-us/library/cc313154(v#office). .12).aspx) dokumentumot a Microsoft.

#### Stream és alfolyam ####

A munkafüzetet a munkafüzet adatfolyam képviseli. A munkafüzet minden munkalapját alfolyamok képviselik. Ezen kívül van diagramlap alfolyama, makrolap alfolyama vagy párbeszédlap alfolyama, amely a globális alfolyamot követi. Minden munkafüzet-adatokat tartalmazó bináris adatfolyamot vagy alfolyamot bináris rekordok sorozataként KELL írni.

#### Rekord ####

A munkafüzet szolgáltatásaira vonatkozó információk rekordként tárolódnak, amely egy változó hosszúságú bájtsorozat. A bináris rekord a következő három összetevőből áll:

**Rekordtípus:** A rekordtípus egy kétbájtos előjel nélküli egész szám, amely meghatározza, hogy a rekord milyen típusú információkat ad meg, és hogyan rendeződik és strukturálja a rekordhoz tartozó rekordadatok szerkezetét. A rekordtípus értékeknek a rekordfelsorolásból (2.3. szakasz) származó értékeknek KELL lenniük, vagy a rekordnak használnia KELL a jövőbeli rekordarchitektúrát (2.1.6. szakasz).

**Rekordméret**: A rekord mérete egy két bájtos előjel nélküli egész szám, amely a rekordadatok teljes méretét meghatározó bájtok számát határozza meg. A rekord méretének 0-nál nagyobbnak vagy egyenlőnek KELL lennie, és 8224-nél kisebbnek vagy egyenlőnek KELL lennie.

**Rekordadatok:** A rekord adatkomponens olyan mezőket tartalmaz, amelyek egy adott rekordtípusnak felelnek meg, és a rekord többi részét alkotják. Az adott rekordtípushoz tartozó mezők sorrendje és szerkezete az adott rekordtípus megfelelő szakaszában van megadva. A rekord adatkomponensének méretének meg kell egyeznie a rekord méretével. A rekord adatkomponens mezői tartalmazhatnak egyszerű értékeket, értéktömböket, több mező struktúráit, mezőtömböket és struktúratömböket.

#### Cellatábla ####

A cellák a munkafüzet alapvető blokkjai, amelyek a munkafüzet tartalmát, például szöveget, képleteket és numerikus adatokat tárolják. A cellák a tárolt adatok nyilvántartását a Cell Table nevű adatszerkezeten keresztül tartják nyilván. Maga a cellatábla a specifikációs dokumentumban meghatározott CELLTABLE szabályoknak megfelelő rekordok sorozatában kerül tárolásra. Sorblokkok sorozatából áll, ahol a sorok sorblokkokba vannak rendezve. Minden sorblokk sorokat tartalmaz az első adatot tartalmazó sortól az utolsó adatot tartalmazó sorig.

Az adatok vagy a sor formázása minden sorblokkhoz sorrekordban kerül mentésre. Minden adatot vagy egyedi cellaformázást tartalmazó cellát egy rekord ábrázol. A cellához társított formázás származhat az egyes cellák formázásából, sorformázásból, oszlopformázásból vagy az alapértelmezett cellaformátumból. A formázás elsőbbségi sorrendje az egyes cellák formázása a legmagasabb prioritással, ezt követi a sorformázás, majd az oszlopformázás, majd az alapértelmezett cellaformátum. Az adatot nem tartalmazó és egyedi formázást nem tartalmazó cellák nem kerülnek mentésre.

#### Képletek ####

A képlet értékek, cellahivatkozások, nevek, függvények vagy operátorok sorozata egy cellában, amelyek együttesen új értéket hoznak létre. A képletek egy tokenizált reprezentációban, úgynevezett "elemzett kifejezésekben" tárolódnak. Az elemzett kifejezés futás közben szöveges képletté alakul a megjelenítés és a felhasználói szerkesztés érdekében. A cellaképleteket a Formula rekord határozza meg. A tömbképleteket az Array rekord határozza meg. A megosztott képleteket az ShrFmla rekord határozza meg.

#### Grafikonok ####

A diagramlap meghatároz egy diagramot, egy grafikát, amely az adatokat vagy az adathalmazok közötti kapcsolatokat vizuális formában jeleníti meg, valamint a diagram adatgyorsítótárát, a diagramadatokban használt adatok helyi másolata hiányzik, vagy ha külső hivatkozások vannak. az adatforrások megszakadtak. A diagram egy vagy kéttengelyes csoportokat határoz meg, egy tengelykészletet, amelyhez a diagramadatokat ábrázolja, valamint a diagramban megadott sorozatokat, trendvonalakat és hibasávot. Minden tengelycsoport egy-négy diagramcsoportot határoz meg, amelyek meghatározzák az adatok megjelenítéséhez használt vizualizáció típusát. Minden sorozat, trendvonal és hibasáv meghatároz egy diagramcsoportot, amelyhez társítva van.

#### Metaadatok ####

A metaadatok egy adott cellához vagy annak tartalmához kapcsolódó további adatok. A metaadatok a BIFF8-ban csak későbbi bővíthetőség céljából kerülnek rögzítésre.

#### Pivot táblák ####

A PivotTable egy olyan mechanizmus, amely a forrásadatok összegzésére szolgál, hogy áttekintést kapjon az adatok elosztásáról. A kimutatásban a forrásadatok megfelelő oszlopai olyan mezőkké válnak, amelyek az adatok összegzésére használhatók. Ha a kimutatás forrásadatai OLAP-forrásadatok, az OLAP-hierarchiák és néhány más OLAP-entitás a kimutatás mezőivé válik.
A kimutatás két fő részből áll, egy PivotCache-ből és egy Kimutatás-tábla nézetből. Egyetlen nem OLAP-os kimutatás-gyorsítótár alapján több kimutatás-nézet is létezhet.

#### Stílusok ####

Ez az áttekintés leírja, hogyan kell megadni a lap (1) celláinak formázási és védelmi információit. A cellaformázás több tulajdonságkészletből áll:

* A betűtípus tulajdonságai (félkövér, dőlt, betűszín, betűméret stb.)
* Kitöltés tulajdonságai (előtérszín, háttérszín, minta, színátmenet stb.)
* Igazítási tulajdonságok (balra, középre, jobbra igazítás stb...)
* A szegély tulajdonságai (bal, jobb, felső, alsó, vastag vagy vékony, szín stb.)
* Szám formázási tulajdonságai (dátum, idő, tizedesjegyek száma stb.)
* Védelmi tulajdonságok (zárt, rejtett stb.)

Ezek a tulajdonságok összességében leírják, hogy egy adott cella hogyan jelenik meg és hogyan nyomtatódik ki.

## Referenciák ##

* [[MS-XLS] – Excel bináris fájlformátum-struktúra](https://msdn.microsoft.com/en-us/library/cc313154(v#office.12).aspx)
* [[MS-CFB] – Összetett fájl bináris fájlformátum](https://msdn.microsoft.com/en-us/library/dd942138.aspx)

