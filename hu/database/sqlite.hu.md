{
  "date" : "2019-12-12",
  "keywords" :[ "SQLite", "extension", "file", "file format", "Database File Type", "Database File Format", "Database Files" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Tudjon meg többet az SQLITE fájlformátumról és az API-król, amelyek SQLITE fájlokat hozhatnak létre és nyithatnak meg.",
  "title" :"SQLite fájlformátum",
  "linktitle" : "SQLITE",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-11-09"
}

## Mi az SQLite fájl?

Az .sqlite kiterjesztésű fájl egy könnyű SQL-adatbázisfájl, amelyet az [SQLite](https://www.sqlite.org/index.html) szoftverrel hoztak létre. Ez egy adatbázis magában egy fájlban, és egy önálló, teljes funkcionalitású, rendkívül megbízható [SQL](/hu/database/sql/) adatbázismotort valósít meg. Az SQLite adatbázisfájlok segítségével gazdag tartalom osztható meg a rendszerek között, ha egyszerűen kicseréli ezeket a fájlokat a hálózaton keresztül. Szinte minden mobil és számítógép az SQLite-ot használja az adatok tárolására és megosztására, és ez a választott fájlformátum a többplatformos alkalmazásokhoz. Kompakt használatának és könnyű használhatóságának köszönhetően más alkalmazásokhoz is csomagban kerül forgalomba. SQLite-összerendelések léteznek olyan programozási nyelvekhez, mint a C, [C#](/hu/programing/cs), [C++](/hu/programing/cpp), [Java](/hu/programing/java/), [PHP](/hu/programing/php/ ), és sokan mások.

## SQLite fájlformátum

Az SQLite valójában egy C-nyelvű könyvtár, amely az SQLite RDBMS-t SQLite fájlformátum használatával valósítja meg. A mindennapos új eszközök fejlődésével a fájlformátum visszafelé kompatibilis maradt a régebbi eszközök fogadása érdekében. Az SQLite fájlformátum az adatok hosszú távú archiválási formátuma.

### Az adatbázisfájl

Az SQLite adatbázist két fájl teljes mértékben karbantartja.
* Fő adatbázis fájl - Az SQLite adatbázis teljes állapotát tartalmazza
* Visszagörgetési napló – További információkat tárol egy második fájlban, és a tranzakciók végrehajtása során használatos. Abban az esetben, ha az SQLite WAL módban van, a rendszer egy írófej naplófájlt tart fenn.

#### Naplófájl

Ennek a fájlnak az a célja, hogy megőrizze az összes karbantartott információt arra az esetre, ha az utolsó tranzakciót nem lehetne végrehajtani, például számítógép-összeomlás esetén. Ez a fájl az adatbázisfájl konzisztens állapotának visszaállítására szolgál.

#### Oldalak

A fő SQLite adatbázisfájl egy vagy több oldalból áll. Bármikor a fő adatbázis minden oldala egyszer használatos, amely a következők egyike:

* A lock-byte oldal
* Egy szabadlistás oldal
* Egy szabadlistás törzsoldal
* Egy szabadlistás levéloldal
* Egy b-fa oldal
* A táblázat b-fa belső oldala
* Egy táblázat b-fa levél oldal
* Egy index b-tree belső oldal
* Egy index b-fa levél oldal
* A rakomány túlcsordulási oldala
* Egy mutató térképoldal

Az SQLite adatbázisfájlok mérete néhány kilobájttól néhány gigabájtig terjedhet.

### SQLite fejléc

Az SQLite adatbázis fejléce az adatbázisfájl első 100 bájtjában található. Minden érvényes SQLite adatbázisfájl 16 bájttal kezdődik (hexadecimálisan):53 51 4c 69 74 65 20 66 6f 72 6d 61 74 20 33 00. A fejlécmezők részletei a következő táblázatban találhatók.

|Eltolás|Méret|Leírás|
---|---|---|
|0|16|A fejléc karakterlánca: "SQLite format 3\000"|
|16|2|Az adatbázis oldal mérete bájtban. Kettő hatványának kell lennie 512 és 32768 között, vagy az 1-es értéknek, amely 65536 oldalméretet jelent.|
|18|1|Fájlformátum írási verziója. 1 a hagyatékhoz; 2 a WAL esetében.|
|19|1|Fájlformátum olvasott verziója. 1 a hagyatékhoz; 2 a WAL esetében.|
|20|1|Bájt kihasználatlan "foglalt" terület minden oldal végén. Általában 0.|
|21|1|Maximális beágyazott hasznos teherhányad. 64.|
|22|1|Minimális beágyazott hasznos teherhányad. 32.|
|23|1|A levél hasznos terhe. 32.|
|24|4|Fájlváltás-számláló.|
|28|4|Az adatbázis fájl mérete oldalakban. A "fejlécben lévő adatbázis mérete".|
|32|4|Az első szabadlista törzsoldalának oldalszáma.|
|36|4|A szabadlistás oldalak száma összesen.|
|40|4|A séma cookie.|
|44|4|A sémaformátum száma. A támogatott sémaformátumok az 1, 2, 3 és 4.|
|48|4|Alapértelmezett oldal-gyorsítótár mérete.|
|52|4|A legnagyobb gyökér b-fa oldalszáma automatikus vákuum vagy növekményes vákuum módban, vagy nulla egyébként.|
|56|4|Az adatbázis szövegkódolása. Az 1-es érték UTF-8-at jelent. A 2-es érték UTF-16le-t jelent. A 3-as érték azt jelenti, hogy UTF-16be.|
|60|4|A user_version pragma által beolvasott és beállított "felhasználói verzió".|
|64|4|Igaz (nem nulla) a növekményes vákuum módhoz. Hamis (nulla) egyébként.|
|68|4|A PRAGMA application_id.| által beállított "Alkalmazásazonosító".
|72|20|Bővítésre fenntartva. Nullának kell lennie.|
|92|4|A verzió érvényes száma.|
|96|4|SQLITE_VERZIÓ_SZÁMA|

## Referenciák ##

* [SQLite fájlformátum – SQLite](https://www.sqlite.org/fileformat2.html)
* [SQLite – Wikipedia](https://en.wikipedia.org/wiki/SQLite)
* [SQLite – C nyelvi specifikációk](https://www.sqlite.org/c3ref/intro.html)

