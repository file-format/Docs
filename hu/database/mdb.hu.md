{
  "date" : "2020-11-11",
  "keywords" :[ "MDB", "kiterjesztés", "fájl", "fájlformátum", "adatbázisfájl típusa", "adatbázisfájlformátum", "adatbázisfájlok" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"További információ az MDB fájlformátumról és az API-król, amelyek MDB fájlokat hozhatnak létre és nyithatnak meg.",
  "title" :"MDB fájlformátum - Microsoft Access adatbázisfájl",
  "linktitle" : "MDB",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-11-11"
}

## Mi az MDB fájl?

Az .mdb kiterjesztésű fájl egy Microsoft Access adatbázisfájl, amely egy relációs adatbázis-kezelő rendszer (RDBMS). Adatbázistáblákban tárolja az adatokat, amelyek elsődleges és idegen kulcsokon keresztül kapcsolódnak egymáshoz. Az MDB fájl tartalmazza az adatbázistáblák teljes szerkezetét, lekérdezéseket, tárolt eljárásokat. Az MDB a Microsoft Access 2003 alapértelmezett fájlformátuma. A Microsoft Access oldalsó verziói az [ACCDB](/hu/database/accdb/) fájlformátumot használják, amely a mai napig a legújabb fájlformátum. Az MDB fájlok megnyithatók olyan alkalmazásokkal, mint a Microsoft Access, MDB Viewer, MDBOpener, és konvertálhatók ACCDB, [CSV](/hu/spreadsheet/csv/), Excel formátumokba stb.

## MDB fájl formátum

Az MDB formátumhoz nyilvános specifikációk állnak rendelkezésre, és ez továbbra is a Microsoft saját fájlformátuma. A Microsoft azonban csatlakozási hozzáférést biztosít az MDB-fájlhoz az Open Database Connectivity (ODBC) szabvány és a Visual Basic for Applications (VBA) használatával. A nem hivatalos MDB útmutató rövid informális leírást ad az MDB formátumról a visszafejtés alapján, és megtekintheti a specifikációkat.

### Oldalak

A nem hivatalos MDB-útmutató szerint az MDB-fájl fix méretű oldalakból áll (2048 bájt a Jeb DB3 és 4096 bájt Jet DB 4 esetén). Az első bájt az oldal típusát jelzi. A legfontosabb oldaltípusok a következők:

`Első oldal:` Adatbázis-fejléc-információkat tartalmaz, amelyek a Jet DB verziójának azonosítását is tartalmazzák, amellyel a fájl kompatibilis. Ezenkívül fájlbiztonsági információkat és az oldalhasználat térképét is tartalmazza.

`Tábladefiníciós oldal:` A táblázatdefiníciós oldal oszlopokat, adattípusokat, indexet és egyéb információkat határoz meg. Szükség esetén további oldalakat használ, és tartalmazza az oldaltérképet, amely tartalmazza a táblázat soradatait.

`Adatoldalak:` Az adatlapok azok a tényleges adattárolók, ahol az adatok soronként kerülnek tárolásra. A hosszú adatértékek tárolására kiegészítő oldalakat használ.

Egyetlen Microsoft Access adatbázis több fájlból is állhat, amelyek lehetővé teszik a fájl- és táblázatméret-korlátozások túllépését. Ez megkönnyíti az űrlapok és kódok elülső MDB-fájlba helyezését a felhasználó asztalán, és adatok elhelyezését egy másik háttér-MDB-fájlban a hálózathoz csatlakoztatott kiszolgálókon.

## Hivatkozások ##

* [Hozzáférési specifikációk](https://support.microsoft.com/en-us/office/access-specifications-0cf3c66f-9cf2-4e32-9568-98c1025bb47c)
