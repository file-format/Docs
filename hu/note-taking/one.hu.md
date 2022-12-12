{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ONE – Microsoft OneNote fájlformátum",
  "description":"További információ az ONE fájlformátumról és az API-król, amelyek EGY fájlt hozhatnak létre és nyithatnak meg.",
  "linktitle" : "ONE",
  "menu" : {
    "docs" : {
      "parent" : "note-taking"
}
},
  "lastmod" : "2019-09-10"
}

## Mi az a .ONE fájl? ##

A .ONE kiterjesztésű fájlokat a Microsoft OneNote alkalmazás hozza létre. A OneNote lehetővé teszi, hogy információkat gyűjtsön az alkalmazás használatával, mintha a vázlatfüzetet használná jegyzetelésre. A OneNote-fájlok különböző elemeket tartalmazhatnak, amelyek nem rögzített helyekre helyezhetők el a dokumentumoldalakon. Ezek az elemek szöveget, digitalizált kézírást és más alkalmazásokból másolt objektumokat tartalmazhatnak, beleértve a képeket, rajzokat és multimédiás (audio/video) klipeket. A Microsoft mostantól az Office365 részeként kínálja a OneNote online verzióját, ahol a jegyzetek megoszthatók más OneNote-felhasználókkal az interneten keresztül.

## .ONE fájlformátum specifikációi ##

A OneNote fájlformátum hatékony módot biztosít a digitális jegyzetek szakaszok és oldalak hierarchikus halmazaként történő megjelenítésére. Minden oldal felhasználó által meghatározott tartalmat tartalmaz egy meghatározott struktúrában, amelyet a fájlformátumú dokumentumobjektum-modell (DOM) ábrázol. Ennek a formátumnak az adatmodellje az alábbi ábrán látható.

### Szerkezet áttekintése ###

A OneNote fájlformátum adatmodelljének megfelelően a OneNote-dokumentumok különböző elemekből állnak.

#### #### szakasz

A szakasz a OneNote-fájl legfelső tárolója, amely további elemeket tartalmaz, például:

* Oldalak
* Metaadatok
* Tulajdonságok

A metaadatok és tulajdonságok magukban foglalják a szakasz nevét, a szakaszban található oldalak azonosítását, valamint az oldalak megjelenési sorrendjét. A "szakasz" kifejezés a szakaszban található összes oldalra és az adatoknak egy OneNote® változattároló fájlban való megjelenítésére vonatkozik, amely .one fájlnévkiterjesztéssel rendelkezik.

#### #### oldal

A OneNote-dokumentum felhasználói által meghatározott tartalma egy oldalon belül található. Az oldalinformációk szöveget, listákat, táblázatokat, oldalcímeket, képeket és jegyzetcímkéket tartalmaznak. Az oldal vázlatobjektumokból áll, amelyekhez a legtöbb benne lévő objektum hozzáadódik. Minden oldalhoz hozzárendelhető egy név az értelmes ábrázoláshoz, és objektumok közvetlenül is hozzáadhatók az oldalakhoz. Egy oldal további aloldalakat tartalmazhat hierarchikus rendszerben.

#### Tulajdonságok és tulajdonságkészletek ####

A OneNote tartalma tulajdonságokból, tulajdonságkészletekből és fájladatobjektumokból áll. A tulajdonságkészlet olyan tulajdonságok gyűjteménye, amelyek valamilyen típusú tartalmat képviselnek. A fájl adatobjektum egy bináris adatblokk, amely képeket, beágyazott fájlokat vagy audio-/videotartalmat tartalmaz.

#### OneNote jegyzetfüzet ####

A jegyzetfüzet olyan szakaszfájlok gyűjteménye, amelyek ugyanabban a könyvtárban vannak tárolva. Tulajdonságok gyűjteménye olyan beállítások megadására szolgál, mint a jegyzetfüzeten belüli szakaszok sorrendje és a jegyzetfüzet színe.

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

`guidFile (16 bájt):` GUID, amely meghatározza ennek a változattároló fájlnak az azonosságát. globálisan egyedinek KELL lennie.

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

|Fájlformátum|Érték
--- | --- |
|.one|0x0000002A
|.onetoc2|0x0000001B

`ffvOldestCodeThatMayReadThisFile (4 bájt):` Előjel nélküli egész szám. A következő táblázatban szereplő értékek egyikének KELL lennie, a fájl fájlformátumától függően.

|Fájlformátum|Érték
--- | --- |
|.one|0x0000002A
|.onetoc2|0x0000001B

`fcrLegacyFreeChunkList (8 bájt):` Egy **FileChunkReference32** struktúra, amelynek "fcrZero" értékkel KELL rendelkeznie.

`fcrLegacyTransactionLog (8 bájt): **FileChunkReference32** struktúra, amelynek "fcrNil"-nek KELL lennie.

`cTransactionsInLog (4 bájt): Előjel nélküli egész szám, amely a tranzakciók számát határozza meg a tranzakciós naplóban. NEM LEHET nulla.

`cbLegacyExpectedFileLength (4 bájt):` Egy előjel nélküli egész szám, amelynek nullának KELL lennie, és figyelmen kívül kell hagyni.

`rgbPlaceholder (8 bájt):` Előjel nélküli egész szám, amelynek nullának KELL lennie, és figyelmen kívül kell hagyni.

`fcrLegacyFileNodeListRoot (8 bájt):` Egy **FileChunkReference32** struktúra, amelynek "fcrNil"-nek KELL lennie.

`cbLegacyFreeSpaceInFreeChunkList (4 bájt): Előjel nélküli egész szám, amelynek nullának KELL lennie, és figyelmen kívül kell hagyni.

`fNeedsDefrag (1 byte):` figyelmen kívül kell hagyni.

`fRepairedFile (1 byte):` figyelmen kívül kell hagyni.

`fNeedsGarbageCollect (1 byte):` figyelmen kívül kell hagyni.

`fHasNoEmbeddedFileObjects (1 bájt):` Egy előjel nélküli egész szám, amelynek nullának KELL lennie, és figyelmen kívül KELL hagyni.

`guidAncestor (16 bájt):` Egy GUID, amely a tartalomjegyzékfájl **Header.guidFile** mezőjét határozza meg, a következő táblázat szerint:


|Tartalomjegyzék-fájl formátuma|Tartalomjegyzék-fájl helye
--- | --- |
|Section File - .One|A tartalomjegyzék fájl ugyanabban a könyvtárban található, mint ez a fájl.
|Tartalomjegyzék fájl - .onetoc2|A tartalomjegyzék fájl a fájl szülőkönyvtárában található.

Ha a GUID azonosító: 00000000-0000-0000-0000-000000000000}, ez a mező nem hivatkozik egy tartalomjegyzék fájlra.

`crcName (4 bájt):` Előjel nélküli egész szám, amely a változattároló fájl nevének CRC értékét adja meg. A név a fájlnév Unicode reprezentációja a kiterjesztésével és egy további null karakterrel a végén. Ezt a CRC-t a rendszer mindig a .one fájl CRC-algoritmusával számítja ki, függetlenül a változattároló fájlformátumtól.

`fcrHashedChunkList (12 bájt): **FileChunkReference64x32** struktúra, amely a kivonatolt csonklista első **FileNodeListFragment** elemére ad hivatkozást. Ha a **FileChunkReference64x32** struktúra értéke "fcrZero" vagy "fcrNil", akkor a kivonatolt darablista nem létezik.

`fcrTransactionLog (12 bájt): **FileChunkReference64x32** struktúra, amely hivatkozást ad meg a tranzakciónapló első **TransactionLogFragment** struktúrájára. Az **fcrTransactionLog** mező értéke NEM lehet "fcrZero" és NEM lehet "fcrNil".

`fcrFileNodeListRoot (12 bájt):` Egy **FileChunkReference64x32** struktúra, amely hivatkozást ad meg egy gyökérfájl csomópontlistájára. Az **fcrFileNodeListRoot** mező értéke NEM lehet "fcrZero" és NEM lehet "fcrNil".

`fcrFreeChunkList (12 bájt): **FileChunkReference64x32** struktúra, amely hivatkozást ad meg az első **FreeChunkListFragment** struktúrára. Ha a **FileChunkReference64x32** struktúra értéke "fcrZero" vagy "fcrNil", akkor a szabad darablista nem létezik.

`cbExpectedFileLength (8 bájt): Előjel nélküli egész szám, amely a változattároló fájl méretét adja meg bájtban.

`cbFreeSpaceInFreeChunkList (8 bájt):` Egy előjel nélküli egész szám, amelynek meg KELL adnia a szabad darablista által megadott szabad terület méretét bájtokban.

`guidFileVersion (16 bájt):` A GUID. Ha a **cTransactionsInLog** mező vagy a **guidDenyReadFileVersion** mező értéke megváltozik, a **guidFileVersion** értéket új GUID-re KELL módosítani.

`nFileVersionGeneration (8 bájt):` Előjel nélküli egész szám, amely megadja, hogy hányszor változott a fájl. Növelni KELL, ha a **guidFileVersion** mező megváltozik.

`guidDenyReadFileVersion (16 bájt):` A GUID. Amikor a fájl meglévő tartalmát módosítják, kivéve a fájl **Header** szerkezetét és a fel nem használt tárolóblokkokat, a **guidDenyReadFileVersion** fájlt új GUID-re KELL módosítani.

`grfDebugLogFlags (4 bájt):` nullának KELL lennie. figyelmen kívül kell hagyni.

`fcrDebugLog (12 bájt):` Egy **FileChunkReference64x32** struktúra, amelynek "fcrZero" értékkel KELL rendelkeznie. figyelmen kívül kell hagyni.

`fcrAllocVerificationFreeChunkList (12 bájt):` Egy **FileChunkReference64x32** struktúra, amelynek "fcrZero"-nak KELL lennie. figyelmen kívül kell hagyni.

`bnCreated (4 bájt):` Előjel nélküli egész szám, amely megadja a változattároló fájlt létrehozó alkalmazás buildszámát. figyelmen kívül KELL hagyni.

`bnLastWroteToThisFile (4 bájt):` Előjel nélküli egész szám, amely megadja annak az alkalmazásnak a build számát, amely utoljára írt ebbe a változattároló fájlba. figyelmen kívül KELL hagyni.

`bnOldestWritten (4 bájt):` Előjel nélküli egész szám, amely a legrégebbi alkalmazás buildszámát adja meg, amely ebbe a változattároló fájlba írt. figyelmen kívül KELL hagyni.

`bnNewestWritten (4 bájt): Előjel nélküli egész szám, amely a legújabb alkalmazás buildszámát adja meg, amely ebbe a változattároló fájlba írt. figyelmen kívül kell hagyni.

`rgbReserved (728 bájt):` nullának KELL lennie. figyelmen kívül kell hagyni.

## Referenciák ##

* [[MS-ONESTORE] – OneNote fájlformátum](https://msdn.microsoft.com/en-us/library/dd951288(v#office.12).aspx)
* [Microsoft OneNote – Wikipedia](https://en.wikipedia.org/wiki/Microsoft_OneNote#References)

