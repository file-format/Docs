{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ONETOC2 – Microsoft OneNote fájlformátum",
  "description":"További információ az ONETOC2 fájlformátumról és az API-król, amelyek ONETOC2 fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "ONETOC2",
  "menu" : {
    "docs" : {
      "parent" : "note-taking"
}
},
  "lastmod" : "2019-09-10"
}

## Mi az ONETOC2? ##

Azok, akik a [Microsoft OneNote](https://products.office.com/en-us/onenote/digital-note-taking-app) alkalmazással dolgoztak, észrevehették .onetoc2 fájlok jelenlétét a notebook mappájában. A Microsoft OneNote bináris .onetoc2 fájlt hoz létre tartalomjegyzékként, hogy indexet tartson a jegyzetfüzet különböző jegyzetelési szakaszainak sorrendjéről. A jegyzetfüzet olyan szakaszfájlok gyűjteménye, amelyek ugyanabban a könyvtárban vannak tárolva. Az .onetoc2 fájl tulajdonságok gyűjteményét használja a beállítások megadására, például a jegyzetfüzeten belüli szakaszok sorrendjére és a jegyzetfüzet színére.

Amikor létrehoz egy jegyzetfüzetet a OneNote 2016-ban, a rendszer automatikusan az új, 2010–2016-os fájlformátumban menti. Erre a formátumra akkor lesz szüksége, ha azt szeretné, hogy a OneNote 2016 összes funkciója – például a matematikai egyenletek és a kapcsolódó jegyzetek – megfelelően működjön.

## ONETOC2 fájlformátum ##

Az .onetoc2 fájlformátum OneNote Revision Store fájlformátumként jelenik meg, és olyan struktúrák gyűjteménye, amelyek kereszthivatkozásokkal ellátott objektumterekbe rendezett változattárolót adnak meg, amelyek tulajdonságkészletekkel rendelkező objektumokat tartalmaznak, és tranzakciós naplót tartalmaznak az aszinkron fájlintegritás biztosítására. írja. Az .onetoc2 fájlformátum teljes specifikációja [online](https://msdn.microsoft.com/en-us/library/dd951288(v#office.12).aspx) érhető el, és az alkalmazások fejlesztésekor hivatkozni lehet rájuk. .

### Fájlszerkezet ###

A változattároló fájlnak **Header** szerkezettel KELL kezdődnie. A fájl többi része bájtos blokkokra van felosztva, ahol az egyes blokkok méretét és szerkezetét a rájuk hivatkozó mező határozza meg. Egy blokk akkor érhető el, ha a **Header** szerkezet hivatkozik rá, vagy ha egy másik elérhető blokk mezője hivatkozik rá. A **Header** struktúrán kívüli adatokat és az elérhető blokkokat figyelmen kívül kell hagyni.

Minden struktúra 1 bájtos határokhoz igazodik. Minden egész szám alá van írva, hacsak nincs másképp megadva. Minden mező [little-endian](https://msdn.microsoft.com/en-us/library/dd773246(v#office.12).aspx#gt_079478cb-f4c5-4ce5-b72b-2144da5d2ce7), hacsak nincs másképp megadva.

#### Fejléc ####

A .ONE fájl fejléce olyan darabokból áll, amelyek különböző egyedi azonosítókat és mezőket tartalmaznak a fájlinformációk megjelenítéséhez, az alábbiak szerint:

`guidFileType (16 bájt):` Egy GUID, amely meghatározza a változattároló fájl típusát. A következő táblázat egyik értékének KELL lennie.

|Fájlformátum|Érték
--- | --- |
|.one|{7B5C52E4-D88C-4DA7-AEB1-5378D02996D3}
|.onetoc2|{43FF2FA1-EFD9-4C76-9EE2-10EA5722765F}

`guidFile (16 bájt):` Egy GUID, amely meghatározza ennek a változattároló fájlnak az azonosságát. globálisan egyedinek KELL lennie.

`guidLegacyFileVersion (16 bájt):` "{00000000-0000-0000-0000-000000000000}" KELL, és figyelmen kívül KELL hagyni.

`guidFileFormat (16 bájt):` Egy GUID, amely meghatározza, hogy a fájl egy változat-tároló fájl. A következőnek KELL lennie: „{109ADD3F-911B-49F5-A5D0-1791EDC8AED8}”.

`ffvLastCodeThatWroteToThisFile (4 bájt):` Egy előjel nélküli egész szám. A fájltípustól függően a következő táblázatban szereplő értékek egyikének KELL lennie.

|Fájlformátum|Érték
--- | --- |
|.one|0x0000002A
|.onetoc2|0x0000001B

`ffvOldestCodeThatHasWrittenToThisFile (4 bájt):` Egy előjel nélküli egész szám. A következő táblázatban szereplő értékek egyikének KELL lennie, a fájl fájlformátumától függően.


|Fájlformátum|Érték
--- | --- |
|.one|0x0000002A
|.onetoc2|0x0000001B

`ffvNewestCodeThatHasWrittenToThisFile (4 bájt):` Egy előjel nélküli egész szám. A következő táblázatban szereplő értékek egyikének KELL lennie, a fájl fájlformátumától függően.
:


|Fájlformátum|Érték
--- | --- |
|.one|0x0000002A
|.onetoc2|0x0000001B

`ffvOldestCodeThatMayReadThisFile (4 bájt):` Előjel nélküli egész szám. A következő táblázatban szereplő értékek egyikének KELL lennie, a fájl fájlformátumától függően.


|Fájlformátum|Érték
--- | --- |
|.one|0x0000002A
|.onetoc2|0x0000001B

## Hivatkozások ##

* [[MS-ONESTORE] – OneNote fájlformátum](https://msdn.microsoft.com/en-us/library/dd951288(v#office.12).aspx)
* [Microsoft OneNote – Wikipedia](https://en.wikipedia.org/wiki/Microsoft_OneNote#References)

