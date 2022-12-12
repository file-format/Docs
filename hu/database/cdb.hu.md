{
  "date" : "2021-06-16",
  "keywords" :[ "CDB", "kiterjesztés", "cdb fájl", "cdb fájlformátum", "adatbázis fájltípus", "adatbázisfájl formátum", "mi az a cdb fájl" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"További információ a CDB fájlformátumról és az API-król, amelyek CDB-fájlok létrehozására és megnyitására képesek.",
  "title" :"CDB - állandó adatbázisfájl",
  "linktitle" : "CDB",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2021-06-16"
}

## Mi az a CDB fájl?
A CDB-fájlokat olyan kritikus alkalmazásokban használják, mint az e-mail. A CDB a "konstans adatbázis" rövidítése, egy gyors, megbízható és egyszerű csomag állandó adatbázisok létrehozásához vagy olvasásához. Az adatbázis-csere biztonságos a rendszerösszeomlás ellen. A felhasználóknak nem kell szünetet tartaniuk az újraírás közben. A CDB asszociatív tömbként (lemezen) működik, leképezi a kulcsokat értékekre, és lehetővé teszi több érték egyetlen kulcsban való tárolását.

## CDB fájl formátum
A CDB fájlformátum a számokat, az eltolásokat, a hosszúságokat és a hash értékeket kis endian formátumban előjel nélküli 32 bites egész számként tárolja. Úgy gondolják, hogy a kulcsok és az adatok átlátszatlan bájtkarakterláncok, különösebb kezelés nélkül. Az adatbázis elején a fix méretű fejléc 256 hash táblát ábrázol, felsorolva a fájlon belüli pozíciójukat és hosszukat a slotokban. Általában az adatokat rekordok sorozataként tárolják, minden rekord tárolja a kulcshosszt, az adathosszt, a kulcsot és az adatokat. Nincsenek rendezési vagy igazítási szabályok. A rekordokat egy 256, változó hosszúságú hash tábla követi. Mivel a nulla érvényes hosszúságú, előfordulhat, hogy az adatbázisban fizikailag kevesebb mint 256 hash tábla van tárolva, de semmi sem tekinthető 256 táblának. A hash táblák egy sor résből állnak, amelyek mindegyike tartalmaz egy hash értéket és egy rekordeltolást. Az „üres helyek” eltolása nulla.

### Szerkezet
A CDB adatbázis egy teljes adatkészletből áll egyetlen számítógépes fájlban. Három részből áll:
- Fix méretű fejléc
- Adatok
- Egy sor hash tábla.

A keresések csak a pontos kulcsokra állnak rendelkezésre. A keresések a következő algoritmus szerint működnek:

- Hash a kulcsot.
- Határozza meg, hogy melyik hash táblában és nyílásban legyen ez a rekord.
- Tesztelje a jelzett nyílást a hash táblázatban.

Egynél több értékkel rendelkező kulcsok keresése esetén további értékeket találhat, ha egyszerűen folytatja a keresést a következő helyen.

#### Jellemzők

A CDB adatbázis-struktúra számos szolgáltatást kínál:

##### Gyors keresések
Egy hatalmas adatbázisban történő sikeres keresés általában csak két lemezelérést igényel, a sikertelen keresés pedig csak egyet.
##### Alacsony rezsi
Egy adatbázis 2048 bájtot, rekordonként 24 bájtot, valamint a kulcsok és adatok számára fenntartott helyet használ.
##### Nincsenek véletlenszerű korlátok
A CDB bármilyen adatbázist képes kezelni 4 gigabájtig. Mivel nincs más korlátozás, a rekordoknak nem is kell beleférniük a memóriába. Az adatbázisokat gépfüggetlen formátumban tárolják.
##### Gyors atomi adatbáziscsere
A **cdbmake** paranccsal egy teljes adatbázist két nagyságrendre lehet átírni, gyorsabban, mint más kivonatoló csomagok.
##### Gyors adatbázis kiíratások
A **cdbdump** képes kinyomtatni az adatbázis tartalmát cdbmake-kompatibilis formátumban.


## Hivatkozások ##

* [cdb (szoftver) - Wikipédia](https://en.wikipedia.org/wiki/Cdb_(szoftver))
* [CDB specifikáció] (http://cr.yp.to/cdb.html)

