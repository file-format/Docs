{
  "date" : "2019-12-09",
  "keywords" :[ "zip fájl", "zip fájl formátum", "mi az a zip fájl", "fájl", "zip-példa", "zip fájl kiterjesztése", "kiterjesztés", "formátum" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"POSTAI IRÁNYÍTÓSZÁM",
  "description":"Mi az a ZIP-fájl és API-k, amelyek ZIP-fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "ZIP",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2019-12-09"
}

## Mi az a ZIP fájl? ##

A .zip kiterjesztésű fájl olyan archívum, amely egy vagy több fájlt vagy könyvtárat tartalmazhat. Az archívum tömörítést alkalmazhat a mellékelt fájlokon a ZIP-fájl méretének csökkentése érdekében. A ZIP fájlformátumot Phil Katz 1989 februárjában tette nyilvánossá a fájlok és mappák archiválása érdekében. A formátum a [PKZIP](https://www.pkware.com/pkzip) segédprogram részévé vált, amelyet a PKWARE, Inc. hozott létre közvetlenül az [elérhető specifikációk](https://pkware.cachefly.net/webdocs/casestudies/APPNOTE.TXT), sok vállalat a ZIP-fájlformátumot tette a segédprogramjai részévé, köztük a Microsoft (Windows 7 óta), az Apple (Mac OS X) és sok más.

## A ZIP fájlformátum rövid története

A ZIP fájlformátum előzményei a System Enhancement Associates (SEA) által a PKWARE ellen indított perig nyúlnak vissza, amiért az ARC segédprogramját a védjegye, valamint a termék megjelenésére és felhasználói felületére vonatkozó szerzői jogok nélkül használta. Ezt megelőzően Phil Katz újraírta a SEA forráskódját, és kiadta a PKXARC-t, egy ARC-kivonatot, valamint a PKARC-ot, egy fájltömörítőt, ingyenes szoftverként MS-DOS alapú rendszerekhez. A pert elvesztve a PKWARE már nem tudta használni az ARC-vel kapcsolatos semmit. Itt jött létre egy új fájltömörítés, a ZIP néven, amely a PKWARE, Inc. PKZIP segédprogramjának részévé vált.

Katz nyilvánosságra hozta a ZIP fájlformátum specifikációit, miközben megtartotta a tulajdonjogát a tömörítő és kivonatoló segédprogramja, azaz a PKZIP felett. A ZIP tömörítési rendszer képes volt (és képes is) archiválni a fájlokat egy mappában egy 32 bites ciklikus redundancia-ellenőrző ([CRC](http://en.wikipedia.org/wiki/Cyclic_redundancy_check)) algoritmus segítségével a fájl tömörítésére. méretek. Az ARC-vel ellentétben a .ZIP mappák tartalmaztak egy könyvtárfájlt, amely a titkosító kódkönyvének szerepét töltötte be, és a tömörített fájlok megjelenítéséhez szükséges információkat tartalmazta.

## Támogatott tömörítési módszerek ZIP-ben

A .ZIP fájlformátum specifikációi szerint a következő tömörítési módszerek támogatottak.

* Tárolás – tömörítés nélkül
* Zsugorodik
* Csökkentés (ez 1-től 4-ig terjedő tömörítési tényezőket jelent)
* Felrobban
* Leereszteni
* Deflat64
* BZIP2
* LZMA (EFS)
* WavPack
* PPMd I-es verzió, 1. változat

A DEFLATE az általánosan használt tömörítési módszer, amely egy veszteségmentes dátumtömörítési algoritmus, amely az LZ77 és a Huffman kódolás kombinációját használja, és amelyet az [RFC 1951](https://tools.ietf.org/html/rfc1951) részletez.

## ZIP fájl formátum specifikációi

A ZIP fájlok több fájl tárolására is képesek különböző tömörítési technikákkal, ugyanakkor támogatják a fájlok tömörítés nélküli tárolását. Minden egyes fájlt külön-külön tárolnak/tömörítenek, ami segít kicsomagolni őket, vagy újakat hozzáadni anélkül, hogy a teljes archívumra tömörítést vagy kicsomagolást alkalmaznának.

### Általános ZIP-fájlformátum

Minden ZIP-fájl a következő módon épül fel:


|ZIP fájlformátum
---|
|Helyi fájl fejléc 1
|Fájladatok 1
|1. adatleíró
|Helyi fájlfejléc 2
|Fájladatok 2
|Adatleíró 2
| ....
| ....
|Helyi fájlfejléc N
|N. fájladatok
|N. adatleíró
|Archív Decryption Header
|Extra adatrekord archiválása
|Központi címtár

A ZIP fájlformátum 32 bites CRC algoritmust használ az archiváláshoz. A tömörített fájlok előállítása érdekében a ZIP archívum egy könyvtárat tartalmaz a végén, amely megőrzi a benne lévő fájlok bejegyzését és az archív fájlban lévő helyüket. Így a kódolás szerepét tölti be a tömörített fájlok megjelenítéséhez szükséges információk beágyazásához. A ZIP-olvasók a könyvtár segítségével töltik be a fájlok listáját anélkül, hogy elolvasnák a teljes ZIP-archívumot. A formátum megőrzi a címtárszerkezet kettős másolatát, hogy nagyobb védelmet nyújtson az adatvesztés ellen.

A ZIP archívumban lévő minden egyes fájl egyedi bejegyzésként jelenik meg, ahol minden bejegyzés egy helyi fájl fejlécből, majd a tömörített fájladatokból áll. Az archívum végén található könyvtár tartalmazza az összes ilyen fájlbejegyzésre vonatkozó hivatkozásokat. A ZIP-fájlolvasóknak kerülniük kell a helyi fájlfejlécek olvasását, és mindenféle fájllistát a könyvtárból kell olvasni. Ez a könyvtár az egyetlen forrás az érvényes fájlbejegyzésekhez az archívumban, mivel a fájlok az archívum vége felé is hozzáfűzhetők. Éppen ezért, ha egy olvasó a ZIP archívum helyi fejléceit a kezdetektől olvassa, akkor az érvénytelen (törölt) bejegyzéseket is olvassa, valamint azokat, amelyek nem részei az archívumból törlendő könyvtárnak.

A központi könyvtár fájlbejegyzéseinek sorrendje nem kell, hogy egyezzen az archívum fájlbejegyzéseinek sorrendjével.

### ZIP fájl bejegyzések

A ZIP-fájl bejegyzései egymás után vannak elrendezve, ahol minden bejegyzés a következőkből áll:

* Helyi fájl fejléc
* Opcionális extra adatmezők
* Felhasználói adatok (opcionálisan tömörítve/opcionálisan titkosítva)

Az egyes bejegyzések helyi fájlfejléce a fájlra vonatkozó információkat, például megjegyzést, fájlméretet és fájlnevet tartalmaz. Az extra adatmezők (opcionális) információkat tartalmazhatnak a ZIP formátum bővíthetőségi lehetőségeiről.

#### Helyi fájl fejléc

A helyi fájlfejlécnek speciális mezőstruktúrája van, amely több bájtos értékekből áll. Az összes érték kis-végi bájt sorrendben kerül tárolásra, ahol a mező hossza a hosszt bájtokban számolja. A ZIP-fájlban lévő összes struktúra 4 bájtos aláírást használ minden fájlbejegyzéshez. A központi címtár aláírásának vége 0x06054b50, és saját egyedi aláírásával lehet megkülönböztetni. A következő a Helyi fájlfejlécben tárolt információk sorrendje.


|Eltolás|Bájtok|Leírás
---|---|---|
|0|4|Helyi fájlfejléc-aláírás # 0x04034b50 (olvasható, mint egy kis szám)
|4|2|Kibontáshoz szükséges verzió (minimum)
|6|2|Általános bitjelző
|8|2|Tömörítési módszer
|10|2|A fájl utolsó módosításának ideje
|12|2|A fájl utolsó módosításának dátuma
|14|4|CRC-32
|18|4|Tömörített méret
|22|4|Tömörítetlen méret
|26|2|Fájlnév hossza (n)
|28|2|Extra mezőhossz (m)
|30|n|Fájlnév
|30+n|m|Extra mező

#### Központi könyvtárfájl fejléce


|Eltolás|Bájtok|Leírás
---|---|---|
|0|4|Központi könyvtárfájl fejléc aláírása # 0x02014b50
|4|2|Verzió: készítette
|6|2|Kibontáshoz szükséges verzió (minimum)
|8|2|Általános bitjelző
|10|2|Tömörítési módszer
|12|2|A fájl utolsó módosításának ideje
|14|2|A fájl utolsó módosításának dátuma
|16|4|CRC-32
|20|4|Tömörített méret
|24|4|Tömörítetlen méret
|28|2|Fájlnév hossza (n)
|30|2|Extra mezőhossz (m)
|32|2|Fájl megjegyzés hossza (k)
|34|2|Lemezszám, ahol a fájl kezdődik
|36|2|Belső fájlattribútumok
|38|4|Külső fájlattribútumok
|42|4|A helyi fájlfejléc relatív eltolása. Ez az első lemez eleje és a helyi fájlfejléc kezdete közötti bájtok száma. Ez lehetővé teszi a központi könyvtárat olvasó szoftver számára, hogy megtalálja a fájl helyét a ZIP-fájlban.
|46|n|Fájlnév
|46+n|m|Extra mező
|46+n+m|k|Fájl megjegyzés

#### A központi címtárrekord vége


|Eltolás|Bájtok|Leírás
---|---|---|
|0|4|A központi címtár aláírásának vége # 0x06054b50
|4|2|A lemez száma
|6|2|Lemez, ahol a központi könyvtár kezdődik
|8|2|A központi címtárrekordok száma ezen a lemezen
|10|2|A központi címtárrekordok száma összesen
|12|4|A központi könyvtár mérete (byte)
|16|4|A központi címtár kezdetének eltolása az archívum kezdetéhez képest
|20|2|Megjegyzés hossza (n)
|22|n|Megjegyzés

## Hivatkozások

* [PKWARE ZIP-fájlformátum specifikációi](https://pkware.cachefly.net/webdocs/casestudies/APPNOTE.TXT)
* [A PKZip-fájl szerkezete](https://users.cs.jmu.edu/buchhofp/forensics/formats/pkzip-printable.html)
