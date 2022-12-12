{
  "date" : "2020-11-11",
  "keywords" :[ "MDF", "kiterjesztés", "fájl", "fájlformátum", "adatbázisfájl típusa", "adatbázisfájlformátum", "adatbázisfájlok" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"További információ az MDF fájlformátumról és az MDF-fájlok létrehozására és megnyitására alkalmas API-król.",
  "title" :"MDF fájlformátum - SQL Server főadatbázisfájl",
  "linktitle" : "MDF",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-08-12"
}

## Mi az MDF fájl?

Az .mdf kiterjesztésű fájl a [Microsoft SQL Server](https://en.wikipedia.org/wiki/Microsoft_SQL_Server) által a felhasználói adatok tárolására használt főadatbázisfájl. Ez rendkívül fontos, mivel minden adat ebben a fájlban van tárolva. Az MDF fájl relációs adatbázisokban tárolja a felhasználók adatait űrlaposzlopokban, sorokban, mezőkben, indexekben, nézetekben és táblázatokban. Az SQL Server lehetővé teszi az automatikus növekedés és az automatikus zsugorítás beállítását, hogy pozitív hatással legyen az adatbázis teljesítményére. Az MDF fájlok a Microsoft SQL Server segítségével tölthetők be és csatolhatók adatbázishoz. Az MDF-fájlok Application/octet-stream MIME típusúak.

## MDF fájl formátum

Az SQL Server adattárolásának alapvető egysége egy oldal. Az adatbázishoz hozzárendelt tárolóoldal 0-tól n-ig sorszámozott logikai oldalakra van felosztva. Egyetlen oldal egy 96 bájtos fejléccel kezdődik, amely tartalmazza az oldalazonosítót, a struktúra típusát, amelyhez az oldal tartozik, az oldalon lévő rekordok számát, valamint az előző és a következő oldalakra mutató mutatókat.

### Fájlszerkezet

Az MDF fájl adatstruktúrája a következő.

* 0. oldal: Fejléc
* 1. oldal: Első PFS
* 2. oldal: Első GAM
* 3. oldal: Első SGAM
* 4. oldal: Nem használt
* 5. oldal: Nem használt
* 6. oldal: Első DCM
* 7. oldal: Első BCM

#### Fájlfejléc

Az összes fájl 0-s oldala tartalmaz egy fejlécet, amely a fájl metaadatait tárolja.

#### Oldal szabad terület (PFS)
A PFS azonosítja a kiosztás állapotát és meghatározza a szabad terület mennyiségét.

* 1. bit: Azt jelzi, hogy az oldal le van-e foglalva vagy sem.
* 2. bit: Azt jelzi, ha az oldal vegyes kiterjedésű.
* 3. bit: azt jelzi, hogy ez az oldal egy IAM oldal.
* 4. bit: Azt jelzi, hogy ez az oldal szellemrekordokat tartalmaz
* 5–7. bit: Kombinált hárombites érték, amely a következőképpen jelzi az oldal teljességét:
* 0: Az oldal üres
* 1: Az oldal 1–50%-ig megtelt
* 2: Az oldal 51–80%-ban megtelt
* 3: Az oldal 81–95%-ban megtelt
* 4: Az oldal 96–100%-ig megtelt

## Hivatkozások

* [Adatbázisfájlok és fájlcsoportok](https://docs.microsoft.com/en-us/sql/relational-databases/databases/database-files-and-filegroups?view=sql-server-ver15)
* [Adatbázis leválasztás és csatolás – SQL Server](https://docs.microsoft.com/en-us/sql/relational-databases/databases/database-detach-and-attach-sql-server?view=sql-server -ver15)
* [Az SQL Server adatfájl-anatómiájának elemzése](https://blog.pythian.com/analyzing-sql-server-data-file-anatomy/)

