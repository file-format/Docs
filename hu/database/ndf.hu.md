{
  "date" : "2020-11-11",
  "keywords" :[ "NDF", "kiterjesztés", "fájl", "fájlformátum", "adatbázisfájl típusa", "adatbázisfájlformátum", "adatbázisfájlok" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"További információ az MDF fájlformátumról és az NDF-fájlok létrehozására és megnyitására alkalmas API-król.",
  "title" :"NDF fájlformátum - SQL Server főadatbázisfájl",
  "linktitle" : "NDF",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-08-12"
}

## Mi az NDF fájl?

Az .ndf kiterjesztésű fájl egy másodlagos adatbázisfájl, amelyet a [Microsoft SQL Server](https://en.wikipedia.org/wiki/Microsoft_SQL_Server) használ felhasználói adatok tárolására. Az NDF egy másodlagos tárolófájl, mivel az SQL-kiszolgáló a felhasználó által megadott adatokat az [MDF] néven ismert elsődleges tárolófájlban tárolja (/hu/database/mdf/). Az NDF-adatfájl nem kötelező, és a felhasználó által meghatározott adattárolás kezelésére szolgál arra az esetre, ha az elsődleges MDF-fájl az összes lefoglalt területet felhasználná. Általában külön lemezen tárolják, és több tárolóeszközre is átterjedhet. Az MDF fájlok jelenléte szükséges az NDF fájlok megnyitásához.

## NDF fájlformátum

Az NDF fájlformátum nem különbözik az [MDF]-től (/hu/database/mdf), és az oldalakat használja az adattárolás alapvető egységeként. minden oldal 96 bájtos fejléccel kezdődik, amely tartalmazza:

* Oldalazonosító
* A szerkezet típusa
* Rekordok száma az oldalakon
* Mutatók az előző és a következő oldalakra

### NDF fájlstruktúra

Az MDF fájl adatstruktúrája a következő.

* 0. oldal: Fejléc
* 1. oldal: Első PFS
* 2. oldal: Első GAM
* 3. oldal: Első SGAM
* 4. oldal: Nem használt
* 5. oldal: Nem használt
* 6. oldal: Első DCM
* 7. oldal: Első BCM

#### NDF-fájl fejléce

Az összes fájl 0-s oldala tartalmaz egy fejlécet, amely a fájl metaadatait tárolja.

#### Oldal szabad terület (PFS)
A PFS azonosítja a kiosztás állapotát és meghatározza a szabad terület mennyiségét.

* 1. bit: Azt jelzi, hogy az oldal le van-e foglalva vagy sem.
* 2. bit: Azt jelzi, ha az oldal vegyes kiterjedésű.
* 3. bit: azt jelzi, hogy ez az oldal egy IAM oldal.
* 4. bit: Azt jelzi, hogy ez az oldal szellemrekordokat tartalmaz
* 5–7. bitek: Kombinált hárombites érték, amely a következőképpen jelzi az oldal teljességét:
* 0: Az oldal üres
* 1: Az oldal 1–50%-ig megtelt
* 2: Az oldal 51–80%-ban megtelt
* 3: Az oldal 81–95%-ban megtelt
* 4: Az oldal 96–100%-ig megtelt

## Adatfájl oldal

Az SQL Server adatfájljában lévő oldalak nulláról (0) kezdődnek, és sorban növekszenek. Minden fájlt egyedi fájlazonosító szám ismer fel. A fájlazonosító és oldalszám pár egyedileg azonosítja az oldalt az adatbázisban. A következő képen látható példa az adatbázis oldalszámainak megjelenítésére.

{{< figure src="../ndf.png" alt="NDF adatbázis fájlformátum" >}}

Ez a példa egy 4 MB-os elsődleges adatfájlt és 1 MB-os másodlagos adatfájlt tartalmazó adatbázis oldalszámait mutatja be.

## Hivatkozások

* [Adatbázisfájlok és fájlcsoportok](https://learn.microsoft.com/en-us/sql/relational-databases/databases/database-files-and-filegroups?view=sql-server-ver16)
* [Adatbázis leválasztás és csatolás – SQL Server](https://learn.microsoft.com/en-us/sql/relational-databases/databases/database-detach-and-attach-sql-server?view=sql-server-ver15)
* [Az SQL Server adatfájl-anatómiájának elemzése](https://blog.pythian.com/analyzing-sql-server-data-file-anatomy/)

